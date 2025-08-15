# VLAN Segmentation Without Trunking (Budget-Friendly Design)  

## **Overview**  
A simple network design using **1 router, 1 switch, and 6 PCs** grouped into 3 VLANs (2 PCs per VLAN) **without trunking**. Ideal for scenarios where:  
- Budget limits advanced switch features.  
- Simplicity is preferred over complex configurations.  
- Security segregation is needed without inter-VLAN routing.  

## **Key Concepts**  
- **No Trunking**: Each VLAN uses a separate physical router interface (no subinterfaces).  
- **Switch Ports**: Access-mode only (no `switchport mode trunk`).  
- **Router-on-a-Stick Alternative**: Avoids the need for a high-end router/switch.  

## **Configuration Files**  
- `notrunkvlan.pkt`: Packet Tracer topology.  
- `Configs/`: Router, switch, and PC configurations.  

## **Why This Design?**  
Trunking requires switches/routers that support 802.1Q, which may not be available in budget setups. This design achieves VLAN isolation with:  
✅ **Lower-cost hardware** (no trunking support needed).  
✅ **Easier troubleshooting** (clear physical separation).  
✅ **Basic security** (VLANs prevent broadcast storms). 

## **Limitations**  
- Scalability (each VLAN requires a physical router port).  
- No inter-VLAN communication (unless configured on the router).  