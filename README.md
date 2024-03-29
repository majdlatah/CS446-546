# CS446/546

## Part 1: Mininet Tutorial ## 

* Prerequisites: Install Mininet & Ryu SDN Controller on your Ubuntu machine.

    1) Mininet: http://mininet.org/download/#option-2-native-installation-from-source
   
       Tree Topology:   
       ```
       sudo mn --controller remote --topo tree,depth=2,fanout=2
       ```
        
       Linear Topology with 2 switches: 
       ```
       sudo mn --controller remote --topo linear,2
       ```
    
       Single Topology with 2 hosts:
       
       ```
       sudo mn --controller remote --topo single,2
       ```
    
    2) Ryu: https://ryu-sdn.org/

* After successful installation, run the SDN controller using ryu-manager with simple switch app: 

    ```
    ryu-manager ryu.app.simple_switch
    ```
     
     To run the controller on a specific port (e.g: __6635__): 
     
     ```
     ryu-manager ryu.app.simple_switch --ofp-tcp-listen-port 6635
     ```
    
* Then, you can run the example you like using python:

  ```
  sudo python low_level_api.py
  ```
