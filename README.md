# Static-Routing-dan-Dynamic-Routing-RIPv2

**TOPOLOGI**

![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/c27ab479-ac00-4080-a320-29f364133107)

# Konfigurasi Static Routing :
- *Router I*
  
  ```
  ROUTER_I (config)#ip route 192.168.20.0 255.255.255.0 10.10.10.2
  ROUTER_I (config)#ip route 10.20.10.0 255.255.255.252 10.10.10.2
  ROUTER_I (config)#ip route 192.168.40.0 255.255.255.0 10.10.10.2
  ```
![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/95d055d7-436c-45be-8f25-a848b5f8345e)

- *Router II*
  
  ```
  ROUTER_II (config)#ip route 192.168.2.0 255.255.255.0 10.10.10.1
  ROUTER_II (config)#ip route 192.168.40.0 255.255.255.0 10.20.10.2
  ```
![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/b4744f22-cef5-46df-a7b8-e7b876707a54)

- *Router III*
  
  ```
  ROUTER_III (config)#ip route 192.168.2.0 255.255.255.0 10.20.10.1
  ROUTER_III (config)#ip route 10.10.10.0 255.255.255.252 10.20.10.1
  ROUTER_III (config)#ip route 192.168.20.0 255.255.255.0 10.20.10.1
  ```
![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/d2dd55fe-640a-408f-ad17-854fce7129ab)

  # Verifikasi Static Routing :

  - *Router I*
  
  ```
  ROUTER_I (config)#show ip route
  ```
![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/08228897-0b68-4a43-a4aa-e817495cff6f)

- *Router II*
  
  ```
  ROUTER_II (config)#show ip route
  ```
  ![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/b0628a07-5d1b-45d2-9c89-16b016ed8ecd)

- *Router III*
  
  ```
  ROUTER_III (config)#show ip route
  ```
  ![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/6173574c-3af2-483b-ac42-3a6d6050ac8b)

    # Konfigurasi Default Routing :

- *Router I*
  
  ```
  ROUTER_I(config)#ip route 0.0.0.0 0.0.0.0 10.10.10.2
  ```
  ![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/1bc56723-7097-4b55-bf51-70432533213a)

- *Router II*
  
  ```
  ROUTER_II(config)#ip route 0.0.0.0 0.0.0.0 10.10.10.1
  ROUTER_II(config)#ip route 0.0.0.0 0.0.0.0 10.20.10.2
  ```
  ![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/07e4c43d-776d-4ba4-8a35-3c3b4541485d)

- *Router III*
  
  ```
  Router_III(config)# ip route 0.0.0.0 0.0.0.0 10.20.10.1
  ```
  ![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/45df3ff8-a0be-4b66-97bd-68edd87dfd9b)

# Konfigurasi Routing Dynamic RIPv2

- *Router I*
  
  ```
  ROUTER_I(config)#router rip
  ROUTER_I(config-router)#version 2
  ROUTER_I(config-router)#network 192.168.2.0
  ROUTER_I(config-router)#network 10.10.10.
  ```
![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/8a51d8a8-8bad-4481-89f0-229873c7749e)

- *Router II*
  
  ```
  ROUTER_II(config)#router rip
  ROUTER_II(config-router)#version 2
  ROUTER_II(config-router)#network 192.168.20.0
  ROUTER_II(config-router)#network 10.10.10.0
  ROUTER_II(config-router)#network 10.20.10.
  ```
![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/dc8ae109-9979-4980-9fc8-a2607aa6bf1e)

- *Router III*
  
  ```
  ROUTER_III(config)#router rip
  ROUTER_III(config-router)#version 2
  ROUTER_III(config-router)#network 192.168.40.0
  ROUTER_III(config-router)#network 10.
  ```
  ![image](https://github.com/eopaleto/Static-Routing-dan-Dynamic-Routing-RIPv2/assets/126212773/34809126-6402-4f35-843f-92dbeb387766)
