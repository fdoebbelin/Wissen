To install and test the **Traefik** on **Windows** without using Docker, you can follow these steps:

## **Step 1: Install with scoop


```
scoop install traefik
```

## **Step 2: Run the Traefik on Powershell**

Type the following command on Powershell once your are in extracted directory


```
traefik version 
```

you can see the following result

![](media/1!gA94YKbJtPe_YQTB7ZgNVQ.png)

## **Step 3. Set Basic Configurations**

a). Now we need to set the configurations , this can be done through either any one

→ Command prompt (CLI)

→ Environment Variables

→ File ( like yaml etc)

b). Let us try with the **_Envionment variables_** option on the powershell and type the following command on the Powershell being in the same directory


```
$env:TRAEFIK_API_INSECURE ='True'
```


and then type **traefik** which is shown in the below code part


```
traefik
```


we can see the following message on Powershell ,

![](media/1!iKeNlaUwo8jnTRVos8YAWQ.png)

c). Incase if you want try through **_configuration file_** , keep the below code in **_.yml file_** and place .yml file in the traefik extracted directory

![](media/1!EKDUTcaDDMDx8kgarfDPgQ.png)


```
traefik.yml
```


and type the following command on Powershell


```
traefik
```


we can see on the Powershell as

**_Configuration loaded from file:_**_downloads/…./traefik.yml_

## **Step 4: Test**

a). Now open [http://localhost:8080/api/overview](http://localhost:8080/api/overview) on any browser or by using postman

![](media/1!CMKwlYc-gsV-jAOYyDzgSg.png)

b). check for the dashboard [http://localhost:8080/dashboard#/](http://localhost:8080/dashboard#/). on browser

![](media/1!4wwmDMb0LObuEGYFWUZTqg.png)

there by downloading , installing ,setting the basic configurations and testing on the browser completed .