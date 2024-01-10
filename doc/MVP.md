# MVP

### 1. Creating ArgoCD app
- Open ArgoCD and click on "NEW APP";
![screenshot](assets/mvp_1.png)

- Enter app name;
- Set "Auto-Create Namepsace" so system will create the new namespace;
![screenshot](assets/mvp_2.png)

- Enter repository URL;
- In the fiels "Path" set path to the helm folder;
![screenshot](assets/mvp_3.png)

- Enter Cluster URL;
- Enter namespace name;
![screenshot](assets/mvp_4.png)

- After configuration click "CREATE"
![screenshot](assets/mvp_5.png)

![screenshot](assets/mvp_6.png)

![screenshot](assets/mvp_7.png)

### 2. App sync
To synchronize application - click on the "SYNC" button. If there are any differents between current and desired states, ArgoCD will sync states.
![screenshot](assets/mvp_8.png)

![screenshot](assets/mvp_9.png)

### 3. Service testing

- Make port forwarding for service
```bash
kubectl port-forward svc/ambassador 8081:80
```
![screenshot](assets/mvp_10.png)

- Run curl to check service
```bash
curl localhost: 8081
```
![screenshot](assets/mvp_11.png)

- Run curl and pass some image into it to use it as a payload

```bash
curl -F 'image=@GithubMark.png' localhost:8088/img/
```
![screenshot](assets/mvp_12.png)


