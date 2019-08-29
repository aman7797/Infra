# 1. Create NFS export & create PV/PVC in OpenShift     && 2. Run application & mount same volume & see if the files are synced

1. Install NFS
2. Create a directory
    
        mkdir practice
3. Make the folder entry in /etc/exports
    
        vi /etc/exports 
4. Add the path of the folder we created above  
![vi code](\img\vim-exports.png)                     and save it  by pressing `Esc+wq`
5. To check the path get exported or not 

    exportfs -r
![vi code](\img\export_check.png)
6. Create `nfs-pv.yaml` file

   ```
    piVersion: v1
    kind: PersistentVolume
    metadata:
    name: nfs-pv-data
    spec:
    capacity:
        storage: 5Gi
    accessModes:
    - ReadWriteOnce
    nfs:
        path: /root/practice
        server: 192.168.110.36
    persistentVolumeReclaimPolicy: Recycle
    ```
    In the file `nfs-pv-data` is the name with which data set is going to be created.   

7. Create `nfs-sql.yaml` file
     
    ```
    piVersion: v1
    kind: PersistentVolumeClaim
    metadata:
    name: nfs-pv-data
    spec:
    accessModes:
        - ReadWriteOnce
    resources:
        requests:
        storage: 1Gi
    ```

8. To create it to the OpenShift
    
        oc create nfs-pv.yaml

9. To create sql file to the OpenShiftoc create      

        nfs-sql.yaml
10. To check if `pv` get created :- 

        get pv
11. To check if `pvc` get created :-

        get pvc
 