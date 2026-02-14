# vmnet Documentation

Source: https://sosumi.ai/documentation/vmnet

---
title: vmnet
source: https://developer.apple.com/documentation/vmnet
timestamp: 2026-02-13T19:03:51.205Z
---

## Essentials

- [com.apple.vm.networking](/documentation/bundleresources/entitlements/com.apple.vm.networking)

## Starting and Stopping Interfaces

- [func vmnet_start_interface(xpc_object_t, dispatch_queue_t, vmnet_start_interface_completion_handler_t) -> interface_ref?](/documentation/vmnet/vmnet_start_interface(_:_:_:))
- [func vmnet_interface_set_event_callback(interface_ref, interface_event_t, dispatch_queue_t?, vmnet_interface_event_callback_t?) -> vmnet_return_t](/documentation/vmnet/vmnet_interface_set_event_callback(_:_:_:_:))
- [func vmnet_stop_interface(interface_ref, dispatch_queue_t, vmnet_interface_completion_handler_t) -> vmnet_return_t](/documentation/vmnet/vmnet_stop_interface(_:_:_:))

## Reading and Writing Packets

- [func vmnet_read(interface_ref, UnsafeMutablePointer<vmpktdesc>, UnsafeMutablePointer<Int32>) -> vmnet_return_t](/documentation/vmnet/vmnet_read(_:_:_:))
- [func vmnet_write(interface_ref, UnsafeMutablePointer<vmpktdesc>, UnsafeMutablePointer<Int32>) -> vmnet_return_t](/documentation/vmnet/vmnet_write(_:_:_:))

## Data Types

- [vmnet_return_t](/documentation/vmnet/vmnet_return_t)

### Constants

- [case VMNET_SUCCESS](/documentation/vmnet/vmnet_return_t/vmnet_success)
- [case VMNET_FAILURE](/documentation/vmnet/vmnet_return_t/vmnet_failure)
- [case VMNET_MEM_FAILURE](/documentation/vmnet/vmnet_return_t/vmnet_mem_failure)
- [case VMNET_INVALID_ARGUMENT](/documentation/vmnet/vmnet_return_t/vmnet_invalid_argument)
- [case VMNET_SETUP_INCOMPLETE](/documentation/vmnet/vmnet_return_t/vmnet_setup_incomplete)
- [case VMNET_INVALID_ACCESS](/documentation/vmnet/vmnet_return_t/vmnet_invalid_access)
- [case VMNET_PACKET_TOO_BIG](/documentation/vmnet/vmnet_return_t/vmnet_packet_too_big)
- [case VMNET_BUFFER_EXHAUSTED](/documentation/vmnet/vmnet_return_t/vmnet_buffer_exhausted)
- [case VMNET_TOO_MANY_PACKETS](/documentation/vmnet/vmnet_return_t/vmnet_too_many_packets)

### Enumeration Cases

- [case VMNET_NOT_AUTHORIZED](/documentation/vmnet/vmnet_return_t/vmnet_not_authorized)
- [case VMNET_SHARING_SERVICE_BUSY](/documentation/vmnet/vmnet_return_t/vmnet_sharing_service_busy)

### Initializers

- [init?(rawValue: UInt32)](/documentation/vmnet/vmnet_return_t/init(rawvalue:))
- [vmpktdesc](/documentation/vmnet/vmpktdesc)

### Fields

- [var vm_flags: UInt32](/documentation/vmnet/vmpktdesc/vm_flags)
- [var vm_pkt_iov: UnsafeMutablePointer<iovec>](/documentation/vmnet/vmpktdesc/vm_pkt_iov)
- [var vm_pkt_iovcnt: UInt32](/documentation/vmnet/vmpktdesc/vm_pkt_iovcnt)
- [var vm_pkt_size: Int](/documentation/vmnet/vmpktdesc/vm_pkt_size)

### Initializers

- [init(vm_pkt_size: Int, vm_pkt_iov: UnsafeMutablePointer<iovec>, vm_pkt_iovcnt: UInt32, vm_flags: UInt32)](/documentation/vmnet/vmpktdesc/init(vm_pkt_size:vm_pkt_iov:vm_pkt_iovcnt:vm_flags:))
- [interface_ref](/documentation/vmnet/interface_ref)
- [interface_event_t](/documentation/vmnet/interface_event_t)

### Constants

- [static var VMNET_INTERFACE_PACKETS_AVAILABLE: interface_event_t](/documentation/vmnet/interface_event_t/vmnet_interface_packets_available)

### Initializers

- [init(rawValue: UInt32)](/documentation/vmnet/interface_event_t/init(rawvalue:))
- [operating_modes_t](/documentation/vmnet/operating_modes_t)

### Constants

- [case VMNET_HOST_MODE](/documentation/vmnet/operating_modes_t/vmnet_host_mode)
- [case VMNET_SHARED_MODE](/documentation/vmnet/operating_modes_t/vmnet_shared_mode)

### Enumeration cases

- [case VMNET_BRIDGED_MODE](/documentation/vmnet/operating_modes_t/vmnet_bridged_mode)

### Initializers

- [init?(rawValue: UInt32)](/documentation/vmnet/operating_modes_t/init(rawvalue:))

## Constants

- [interface_desc XPC Dictionary Keys](/documentation/vmnet/interface_desc_xpc_dictionary_keys)

### Constants

- [let vmnet_operation_mode_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_operation_mode_key)
- [let vmnet_interface_id_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_interface_id_key)
- [interface_param XPC Dictionary Keys](/documentation/vmnet/interface_param_xpc_dictionary_keys)

### Constants

- [let vmnet_mac_address_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_mac_address_key)
- [let vmnet_mtu_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_mtu_key)
- [let vmnet_max_packet_size_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_max_packet_size_key)
- [event XPC Dictionary](/documentation/vmnet/event_xpc_dictionary)

### Constants

- [let vmnet_estimated_packets_available_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_estimated_packets_available_key)

## Reference

- [vmnet Constants](/documentation/vmnet/vmnet_constants)

### Constants

- [let vmnet_allocate_mac_address_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_allocate_mac_address_key)
- [let vmnet_enable_checksum_offload_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_enable_checksum_offload_key)
- [let vmnet_enable_isolation_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_enable_isolation_key)
- [let vmnet_enable_tso_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_enable_tso_key)
- [let vmnet_end_address_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_end_address_key)
- [let vmnet_host_ip_address_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_host_ip_address_key)
- [let vmnet_host_ipv6_address_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_host_ipv6_address_key)
- [let vmnet_host_subnet_mask_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_host_subnet_mask_key)
- [let vmnet_nat66_prefix_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_nat66_prefix_key)
- [let vmnet_nat66_prefix_length_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_nat66_prefix_length_key)
- [let vmnet_network_identifier_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_network_identifier_key)
- [let vmnet_shared_interface_name_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_shared_interface_name_key)
- [let vmnet_start_address_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_start_address_key)
- [let vmnet_subnet_mask_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_subnet_mask_key)
- [vmnet Functions](/documentation/vmnet/vmnet_functions)

### Functions

- [func vmnet_copy_shared_interface_list() -> xpc_object_t?](/documentation/vmnet/vmnet_copy_shared_interface_list())
- [func vmnet_interface_add_ip_port_forwarding_rule(interface_ref, UInt8, UInt16, UInt8, UnsafeRawPointer, UInt16, vmnet_interface_completion_handler_t?) -> vmnet_return_t](/documentation/vmnet/vmnet_interface_add_ip_port_forwarding_rule(_:_:_:_:_:_:_:))
- [func vmnet_interface_add_port_forwarding_rule(interface_ref, UInt8, UInt16, in_addr, UInt16, vmnet_interface_completion_handler_t?) -> vmnet_return_t](/documentation/vmnet/vmnet_interface_add_port_forwarding_rule(_:_:_:_:_:_:))
- [func vmnet_interface_get_ip_port_forwarding_rules(interface_ref, UInt8, vmnet_interface_get_ip_port_forwarding_rules_handler_t) -> vmnet_return_t](/documentation/vmnet/vmnet_interface_get_ip_port_forwarding_rules(_:_:_:))
- [func vmnet_interface_get_port_forwarding_rules(interface_ref, vmnet_interface_get_port_forwarding_rules_handler_t) -> vmnet_return_t](/documentation/vmnet/vmnet_interface_get_port_forwarding_rules(_:_:))
- [func vmnet_interface_remove_ip_port_forwarding_rule(interface_ref, UInt8, UInt16, UInt8, vmnet_interface_completion_handler_t?) -> vmnet_return_t](/documentation/vmnet/vmnet_interface_remove_ip_port_forwarding_rule(_:_:_:_:_:))
- [func vmnet_interface_remove_port_forwarding_rule(interface_ref, UInt8, UInt16, vmnet_interface_completion_handler_t?) -> vmnet_return_t](/documentation/vmnet/vmnet_interface_remove_port_forwarding_rule(_:_:_:_:))
- [func vmnet_ip_port_forwarding_rule_get_details(xpc_object_t, UnsafeMutablePointer<UInt8>, UnsafeMutablePointer<UInt16>, UInt8, UnsafeMutableRawPointer, UnsafeMutablePointer<UInt16>) -> vmnet_return_t](/documentation/vmnet/vmnet_ip_port_forwarding_rule_get_details(_:_:_:_:_:_:))
- [func vmnet_port_forwarding_rule_get_details(xpc_object_t, UnsafeMutablePointer<UInt8>, UnsafeMutablePointer<UInt16>, UnsafeMutablePointer<in_addr>, UnsafeMutablePointer<UInt16>) -> vmnet_return_t](/documentation/vmnet/vmnet_port_forwarding_rule_get_details(_:_:_:_:_:))
- [vmnet Data Types](/documentation/vmnet/vmnet_data_types)

### Data types

- [vmnet_interface_completion_handler_t](/documentation/vmnet/vmnet_interface_completion_handler_t)
- [vmnet_interface_event_callback_t](/documentation/vmnet/vmnet_interface_event_callback_t)
- [vmnet_interface_get_ip_port_forwarding_rules_handler_t](/documentation/vmnet/vmnet_interface_get_ip_port_forwarding_rules_handler_t)
- [vmnet_interface_get_port_forwarding_rules_handler_t](/documentation/vmnet/vmnet_interface_get_port_forwarding_rules_handler_t)
- [vmnet_start_interface_completion_handler_t](/documentation/vmnet/vmnet_start_interface_completion_handler_t)

## Variables

- [let vmnet_enable_virtio_header_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_enable_virtio_header_key-swift.var)
- [let vmnet_read_max_packets_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_read_max_packets_key)
- [let vmnet_write_max_packets_key: UnsafePointer<CChar>](/documentation/vmnet/vmnet_write_max_packets_key)

## Functions

- [func vmnet_interface_start_with_network(vmnet_network_ref, xpc_object_t, dispatch_queue_t, vmnet_start_interface_completion_handler_t) -> interface_ref?](/documentation/vmnet/vmnet_interface_start_with_network(_:_:_:_:))
- [func vmnet_network_configuration_add_dhcp_reservation(vmnet_network_configuration_ref, UnsafePointer<ether_addr_t>, UnsafePointer<in_addr>) -> vmnet_return_t](/documentation/vmnet/vmnet_network_configuration_add_dhcp_reservation(_:_:_:))
- [func vmnet_network_configuration_add_port_forwarding_rule(vmnet_network_configuration_ref, UInt8, sa_family_t, UInt16, UInt16, UnsafeRawPointer) -> vmnet_return_t](/documentation/vmnet/vmnet_network_configuration_add_port_forwarding_rule(_:_:_:_:_:_:))
- [func vmnet_network_configuration_create(vmnet_mode_t, UnsafeMutablePointer<vmnet_return_t>?) -> vmnet_network_configuration_ref?](/documentation/vmnet/vmnet_network_configuration_create(_:_:))
- [func vmnet_network_configuration_disable_dhcp(vmnet_network_configuration_ref)](/documentation/vmnet/vmnet_network_configuration_disable_dhcp(_:))
- [func vmnet_network_configuration_disable_dns_proxy(vmnet_network_configuration_ref)](/documentation/vmnet/vmnet_network_configuration_disable_dns_proxy(_:))
- [func vmnet_network_configuration_disable_nat44(vmnet_network_configuration_ref)](/documentation/vmnet/vmnet_network_configuration_disable_nat44(_:))
- [func vmnet_network_configuration_disable_nat66(vmnet_network_configuration_ref)](/documentation/vmnet/vmnet_network_configuration_disable_nat66(_:))
- [func vmnet_network_configuration_disable_router_advertisement(vmnet_network_configuration_ref)](/documentation/vmnet/vmnet_network_configuration_disable_router_advertisement(_:))
- [func vmnet_network_configuration_set_external_interface(vmnet_network_configuration_ref, UnsafePointer<CChar>) -> vmnet_return_t](/documentation/vmnet/vmnet_network_configuration_set_external_interface(_:_:))
- [func vmnet_network_configuration_set_ipv4_subnet(vmnet_network_configuration_ref, UnsafePointer<in_addr>, UnsafePointer<in_addr>) -> vmnet_return_t](/documentation/vmnet/vmnet_network_configuration_set_ipv4_subnet(_:_:_:))
- [func vmnet_network_configuration_set_ipv6_prefix(vmnet_network_configuration_ref, UnsafePointer<in6_addr>, UInt8) -> vmnet_return_t](/documentation/vmnet/vmnet_network_configuration_set_ipv6_prefix(_:_:_:))
- [func vmnet_network_configuration_set_mtu(vmnet_network_configuration_ref, UInt32) -> vmnet_return_t](/documentation/vmnet/vmnet_network_configuration_set_mtu(_:_:))
- [func vmnet_network_copy_serialization(vmnet_network_ref, UnsafeMutablePointer<vmnet_return_t>?) -> xpc_object_t?](/documentation/vmnet/vmnet_network_copy_serialization(_:_:))
- [func vmnet_network_create(vmnet_network_configuration_ref, UnsafeMutablePointer<vmnet_return_t>?) -> vmnet_network_ref?](/documentation/vmnet/vmnet_network_create(_:_:))
- [func vmnet_network_create_with_serialization(xpc_object_t, UnsafeMutablePointer<vmnet_return_t>?) -> vmnet_network_ref?](/documentation/vmnet/vmnet_network_create_with_serialization(_:_:))
- [func vmnet_network_get_ipv4_subnet(vmnet_network_ref, UnsafeMutablePointer<in_addr>, UnsafeMutablePointer<in_addr>)](/documentation/vmnet/vmnet_network_get_ipv4_subnet(_:_:_:))
- [func vmnet_network_get_ipv6_prefix(vmnet_network_ref, UnsafeMutablePointer<in6_addr>, UnsafeMutablePointer<UInt8>)](/documentation/vmnet/vmnet_network_get_ipv6_prefix(_:_:_:))

## Type Aliases

- [vmnet_mode_t](/documentation/vmnet/vmnet_mode_t)
- [vmnet_network_configuration_ref](/documentation/vmnet/vmnet_network_configuration_ref)
- [vmnet_network_ref](/documentation/vmnet/vmnet_network_ref)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
