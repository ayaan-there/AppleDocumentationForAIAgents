# GSS Documentation

Source: https://sosumi.ai/documentation/gss

---
title: GSS
source: https://developer.apple.com/documentation/gss
timestamp: 2026-02-13T18:57:44.769Z
---

## Memory and Context

- [Allocating and Releasing Objects](/documentation/gss/allocating-and-releasing-objects)
- [Function Status](/documentation/gss/function-status)

### Status and Error Creation

- [OM_uint32](/documentation/gss/om_uint32)
- [OM_uint64](/documentation/gss/om_uint64)
- [gss_uint32](/documentation/gss/gss_uint32)
- [gss_status_id_t](/documentation/gss/gss_status_id_t)
- [var GSS_C_MECH_CODE: Int32](/documentation/gss/gss_c_mech_code)
- [var GSS_C_GSS_CODE: Int32](/documentation/gss/gss_c_gss_code)
- [var GSS_S_COMPLETE: Int32](/documentation/gss/gss_s_complete)
- [func gss_display_status(UnsafeMutablePointer<OM_uint32>, OM_uint32, Int32, gss_OID?, UnsafeMutablePointer<OM_uint32>, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_display_status(_:_:_:_:_:_:))
- [func GSSCreateError(gss_const_OID, OM_uint32, OM_uint32) -> Unmanaged<CFError>?](/documentation/gss/gsscreateerror(_:_:_:))

### Calling Errors

- [var GSS_S_CALL_BAD_STRUCTURE: UInt](/documentation/gss/gss_s_call_bad_structure)
- [var GSS_S_CALL_INACCESSIBLE_READ: UInt](/documentation/gss/gss_s_call_inaccessible_read)
- [var GSS_S_CALL_INACCESSIBLE_WRITE: UInt](/documentation/gss/gss_s_call_inaccessible_write)

### Routine Errors

- [var GSS_S_BAD_MECH: UInt](/documentation/gss/gss_s_bad_mech)
- [var GSS_S_BAD_NAME: UInt](/documentation/gss/gss_s_bad_name)
- [var GSS_S_BAD_NAMETYPE: UInt](/documentation/gss/gss_s_bad_nametype)
- [var GSS_S_BAD_MIC: UInt](/documentation/gss/gss_s_bad_mic)
- [var GSS_S_BAD_SIG: UInt](/documentation/gss/gss_s_bad_sig)
- [var GSS_S_BAD_STATUS: UInt](/documentation/gss/gss_s_bad_status)
- [var GSS_S_BAD_BINDINGS: UInt](/documentation/gss/gss_s_bad_bindings)
- [var GSS_S_NO_CRED: UInt](/documentation/gss/gss_s_no_cred)
- [var GSS_S_NO_CONTEXT: UInt](/documentation/gss/gss_s_no_context)
- [var GSS_S_DEFECTIVE_TOKEN: UInt](/documentation/gss/gss_s_defective_token)
- [var GSS_S_DEFECTIVE_CREDENTIAL: UInt](/documentation/gss/gss_s_defective_credential)
- [var GSS_S_CREDENTIALS_EXPIRED: UInt](/documentation/gss/gss_s_credentials_expired)
- [var GSS_S_CONTEXT_EXPIRED: UInt](/documentation/gss/gss_s_context_expired)
- [var GSS_S_FAILURE: UInt](/documentation/gss/gss_s_failure)
- [var GSS_S_BAD_QOP: UInt](/documentation/gss/gss_s_bad_qop)
- [var GSS_S_UNAUTHORIZED: UInt](/documentation/gss/gss_s_unauthorized)
- [var GSS_S_UNAVAILABLE: UInt](/documentation/gss/gss_s_unavailable)
- [var GSS_S_DUPLICATE_ELEMENT: UInt](/documentation/gss/gss_s_duplicate_element)
- [var GSS_S_NAME_NOT_MN: UInt](/documentation/gss/gss_s_name_not_mn)
- [var GSS_S_BAD_MECH_ATTR: UInt](/documentation/gss/gss_s_bad_mech_attr)
- [var GSS_S_CRED_UNAVAIL: UInt](/documentation/gss/gss_s_cred_unavail)

### Masks and Offsets

- [var GSS_C_CALLING_ERROR_MASK: UInt](/documentation/gss/gss_c_calling_error_mask)
- [var GSS_C_CALLING_ERROR_OFFSET: Int32](/documentation/gss/gss_c_calling_error_offset)
- [var GSS_C_ROUTINE_ERROR_MASK: UInt](/documentation/gss/gss_c_routine_error_mask)
- [var GSS_C_ROUTINE_ERROR_OFFSET: Int32](/documentation/gss/gss_c_routine_error_offset)
- [var GSS_C_SUPPLEMENTARY_MASK: UInt](/documentation/gss/gss_c_supplementary_mask)
- [var GSS_C_SUPPLEMENTARY_OFFSET: Int32](/documentation/gss/gss_c_supplementary_offset)
- [Buffer Management](/documentation/gss/buffer-management)

### Buffer Data Structures

- [gss_qop_t](/documentation/gss/gss_qop_t)
- [gss_iov_buffer_t](/documentation/gss/gss_iov_buffer_t)
- [gss_iov_buffer_desc](/documentation/gss/gss_iov_buffer_desc)

#### Vectored I/O

- [var buffer: gss_buffer_desc](/documentation/gss/gss_iov_buffer_desc_struct/buffer)
- [var type: OM_uint32](/documentation/gss/gss_iov_buffer_desc_struct/type)
- [gss_iov_buffer_desc_struct](/documentation/gss/gss_iov_buffer_desc_struct)

#### Instance Properties

- [var buffer: gss_buffer_desc](/documentation/gss/gss_iov_buffer_desc_struct/buffer)
- [var type: OM_uint32](/documentation/gss/gss_iov_buffer_desc_struct/type)

#### Initialization

- [init()](/documentation/gss/gss_iov_buffer_desc_struct/init())
- [init(type: OM_uint32, buffer: gss_buffer_desc)](/documentation/gss/gss_iov_buffer_desc_struct/init(type:buffer:))
- [gss_buffer_t](/documentation/gss/gss_buffer_t)
- [gss_const_buffer_t](/documentation/gss/gss_const_buffer_t)
- [gss_buffer_set_t](/documentation/gss/gss_buffer_set_t)
- [gss_buffer_desc](/documentation/gss/gss_buffer_desc)

#### Instance Properties

- [var length: Int](/documentation/gss/gss_buffer_desc_struct/length)
- [var value: UnsafeMutableRawPointer!](/documentation/gss/gss_buffer_desc_struct/value)
- [gss_buffer_desc_struct](/documentation/gss/gss_buffer_desc_struct)

#### Instance Properties

- [var length: Int](/documentation/gss/gss_buffer_desc_struct/length)
- [var value: UnsafeMutableRawPointer!](/documentation/gss/gss_buffer_desc_struct/value)

#### Initialization

- [init()](/documentation/gss/gss_buffer_desc_struct/init())
- [init(length: Int, value: UnsafeMutableRawPointer!)](/documentation/gss/gss_buffer_desc_struct/init(length:value:))
- [gss_buffer_set_desc](/documentation/gss/gss_buffer_set_desc)

#### Instance Properties

- [var count: Int](/documentation/gss/gss_buffer_set_desc_struct/count)
- [var elements: UnsafeMutablePointer<gss_buffer_desc>!](/documentation/gss/gss_buffer_set_desc_struct/elements)
- [gss_buffer_set_desc_struct](/documentation/gss/gss_buffer_set_desc_struct)

#### Instance Properties

- [var count: Int](/documentation/gss/gss_buffer_set_desc_struct/count)
- [var elements: UnsafeMutablePointer<gss_buffer_desc>!](/documentation/gss/gss_buffer_set_desc_struct/elements)

#### Initialization

- [init()](/documentation/gss/gss_buffer_set_desc_struct/init())
- [init(count: Int, elements: UnsafeMutablePointer<gss_buffer_desc>!)](/documentation/gss/gss_buffer_set_desc_struct/init(count:elements:))

### Allocation and Deallocation

- [func gss_create_empty_buffer_set(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_buffer_set_t?>) -> OM_uint32](/documentation/gss/gss_create_empty_buffer_set(_:_:))
- [func gss_add_buffer_set_member(UnsafeMutablePointer<OM_uint32>, gss_buffer_t, UnsafeMutablePointer<gss_buffer_set_t>) -> OM_uint32](/documentation/gss/gss_add_buffer_set_member(_:_:_:))
- [func gss_release_buffer(UnsafeMutablePointer<OM_uint32>, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_release_buffer(_:_:))
- [func gss_release_buffer_set(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_buffer_set_t?>) -> OM_uint32](/documentation/gss/gss_release_buffer_set(_:_:))
- [Context Services](/documentation/gss/context-services)

### Flags

- [var GSS_C_DELEG_FLAG: Int32](/documentation/gss/gss_c_deleg_flag)
- [var GSS_C_MUTUAL_FLAG: Int32](/documentation/gss/gss_c_mutual_flag)
- [var GSS_C_REPLAY_FLAG: Int32](/documentation/gss/gss_c_replay_flag)
- [var GSS_C_SEQUENCE_FLAG: Int32](/documentation/gss/gss_c_sequence_flag)
- [var GSS_C_CONF_FLAG: Int32](/documentation/gss/gss_c_conf_flag)
- [var GSS_C_INTEG_FLAG: Int32](/documentation/gss/gss_c_integ_flag)
- [var GSS_C_ANON_FLAG: Int32](/documentation/gss/gss_c_anon_flag)
- [var GSS_C_PROT_READY_FLAG: Int32](/documentation/gss/gss_c_prot_ready_flag)
- [var GSS_C_TRANS_FLAG: Int32](/documentation/gss/gss_c_trans_flag)
- [var GSS_C_DCE_STYLE: Int32](/documentation/gss/gss_c_dce_style)
- [var GSS_C_IDENTIFY_FLAG: Int32](/documentation/gss/gss_c_identify_flag)
- [var GSS_C_EXTENDED_ERROR_FLAG: Int32](/documentation/gss/gss_c_extended_error_flag)
- [var GSS_C_DELEG_POLICY_FLAG: Int32](/documentation/gss/gss_c_deleg_policy_flag)

### Address Families

- [var GSS_C_AF_NS: Int32](/documentation/gss/gss_c_af_ns)
- [var GSS_C_AF_BSC: Int32](/documentation/gss/gss_c_af_bsc)
- [var GSS_C_AF_DLI: Int32](/documentation/gss/gss_c_af_dli)
- [var GSS_C_AF_DSS: Int32](/documentation/gss/gss_c_af_dss)
- [var GSS_C_AF_LAT: Int32](/documentation/gss/gss_c_af_lat)
- [var GSS_C_AF_NBS: Int32](/documentation/gss/gss_c_af_nbs)
- [var GSS_C_AF_OSI: Int32](/documentation/gss/gss_c_af_osi)
- [var GSS_C_AF_PUP: Int32](/documentation/gss/gss_c_af_pup)
- [var GSS_C_AF_SNA: Int32](/documentation/gss/gss_c_af_sna)
- [var GSS_C_AF_X25: Int32](/documentation/gss/gss_c_af_x25)
- [var GSS_C_AF_ECMA: Int32](/documentation/gss/gss_c_af_ecma)
- [var GSS_C_AF_INET: Int32](/documentation/gss/gss_c_af_inet)
- [var GSS_C_AF_CCITT: Int32](/documentation/gss/gss_c_af_ccitt)
- [var GSS_C_AF_CHAOS: Int32](/documentation/gss/gss_c_af_chaos)
- [var GSS_C_AF_INET6: Int32](/documentation/gss/gss_c_af_inet6)
- [var GSS_C_AF_LOCAL: Int32](/documentation/gss/gss_c_af_local)
- [var GSS_C_AF_DECnet: Int32](/documentation/gss/gss_c_af_decnet)
- [var GSS_C_AF_HYLINK: Int32](/documentation/gss/gss_c_af_hylink)
- [var GSS_C_AF_UNSPEC: Int32](/documentation/gss/gss_c_af_unspec)
- [var GSS_C_AF_DATAKIT: Int32](/documentation/gss/gss_c_af_datakit)
- [var GSS_C_AF_IMPLINK: Int32](/documentation/gss/gss_c_af_implink)
- [var GSS_C_AF_NULLADDR: Int32](/documentation/gss/gss_c_af_nulladdr)
- [var GSS_C_AF_APPLETALK: Int32](/documentation/gss/gss_c_af_appletalk)

### Apple Source App Keys

- [var kGSSICAppleSourceAppPID: String](/documentation/gss/kgssicapplesourceapppid)
- [var kGSSICAppleSourceAppAuditToken: String](/documentation/gss/kgssicapplesourceappaudittoken)
- [var kGSSICAppleSourceAppSigningIdentity: String](/documentation/gss/kgssicapplesourceappsigningidentity)

### Channel Bindings

- [gss_ctx_id_t](/documentation/gss/gss_ctx_id_t)
- [gss_channel_bindings_struct](/documentation/gss/gss_channel_bindings_struct)

#### Instance Properties

- [var initiator_addrtype: OM_uint32](/documentation/gss/gss_channel_bindings_struct/initiator_addrtype)
- [var initiator_address: gss_buffer_desc](/documentation/gss/gss_channel_bindings_struct/initiator_address)
- [var acceptor_addrtype: OM_uint32](/documentation/gss/gss_channel_bindings_struct/acceptor_addrtype)
- [var acceptor_address: gss_buffer_desc](/documentation/gss/gss_channel_bindings_struct/acceptor_address)
- [var application_data: gss_buffer_desc](/documentation/gss/gss_channel_bindings_struct/application_data)

#### Initialization

- [init()](/documentation/gss/gss_channel_bindings_struct/init())
- [init(initiator_addrtype: OM_uint32, initiator_address: gss_buffer_desc, acceptor_addrtype: OM_uint32, acceptor_address: gss_buffer_desc, application_data: gss_buffer_desc)](/documentation/gss/gss_channel_bindings_struct/init(initiator_addrtype:initiator_address:acceptor_addrtype:acceptor_address:application_data:))
- [gss_channel_bindings_t](/documentation/gss/gss_channel_bindings_t)

#### Instance Properties

- [var acceptor_address: gss_buffer_desc](/documentation/gss/gss_channel_bindings_struct/acceptor_address)
- [var acceptor_addrtype: OM_uint32](/documentation/gss/gss_channel_bindings_struct/acceptor_addrtype)
- [var application_data: gss_buffer_desc](/documentation/gss/gss_channel_bindings_struct/application_data)
- [var initiator_address: gss_buffer_desc](/documentation/gss/gss_channel_bindings_struct/initiator_address)
- [var initiator_addrtype: OM_uint32](/documentation/gss/gss_channel_bindings_struct/initiator_addrtype)
- [gss_const_channel_bindings_t](/documentation/gss/gss_const_channel_bindings_t)

### Creation and Deletion

- [func gss_init_sec_context(UnsafeMutablePointer<OM_uint32>, gss_cred_id_t?, UnsafeMutablePointer<gss_ctx_id_t?>, gss_name_t, gss_OID?, OM_uint32, OM_uint32, gss_channel_bindings_t?, gss_buffer_t?, UnsafeMutablePointer<gss_OID?>?, gss_buffer_t, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<OM_uint32>?) -> OM_uint32](/documentation/gss/gss_init_sec_context(_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func gss_accept_sec_context(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_ctx_id_t?>, gss_cred_id_t?, gss_buffer_t?, gss_channel_bindings_t?, UnsafeMutablePointer<gss_name_t?>?, UnsafeMutablePointer<gss_OID?>?, gss_buffer_t, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<gss_cred_id_t?>?) -> OM_uint32](/documentation/gss/gss_accept_sec_context(_:_:_:_:_:_:_:_:_:_:_:))
- [func gss_delete_sec_context(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_ctx_id_t?>, gss_buffer_t?) -> OM_uint32](/documentation/gss/gss_delete_sec_context(_:_:_:))
- [func gss_release_cred(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_cred_id_t?>) -> OM_uint32](/documentation/gss/gss_release_cred(_:_:))
- [func gss_process_context_token(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_process_context_token(_:_:_:))
- [func gss_set_sec_context_option(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_ctx_id_t>?, gss_OID, gss_buffer_t?) -> OM_uint32](/documentation/gss/gss_set_sec_context_option(_:_:_:_:))

### Inquiry and Limits

- [func gss_context_time(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, UnsafeMutablePointer<OM_uint32>) -> OM_uint32](/documentation/gss/gss_context_time(_:_:_:))
- [func gss_inquire_context(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, UnsafeMutablePointer<gss_name_t?>?, UnsafeMutablePointer<gss_name_t?>?, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<gss_OID?>?, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<Int32>?, UnsafeMutablePointer<Int32>?) -> OM_uint32](/documentation/gss/gss_inquire_context(_:_:_:_:_:_:_:_:_:))
- [func gss_inquire_sec_context_by_oid(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, gss_OID, UnsafeMutablePointer<gss_buffer_set_t>?) -> OM_uint32](/documentation/gss/gss_inquire_sec_context_by_oid(_:_:_:_:))
- [func gss_wrap_size_limit(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, Int32, gss_qop_t, OM_uint32, UnsafeMutablePointer<OM_uint32>) -> OM_uint32](/documentation/gss/gss_wrap_size_limit(_:_:_:_:_:_:))

### Import and Export

- [func gss_export_sec_context(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_ctx_id_t?>, gss_buffer_t?) -> OM_uint32](/documentation/gss/gss_export_sec_context(_:_:_:))
- [func gss_import_sec_context(UnsafeMutablePointer<OM_uint32>, gss_buffer_t, UnsafeMutablePointer<gss_ctx_id_t?>) -> OM_uint32](/documentation/gss/gss_import_sec_context(_:_:_:))

## Credentials

- [Credential Management](/documentation/gss/credential-management)

### Allocation and Deallocation

- [func GSSCreateCredentialFromUUID(CFUUID) -> gss_cred_id_t?](/documentation/gss/gsscreatecredentialfromuuid(_:))
- [func gss_add_cred(UnsafeMutablePointer<OM_uint32>, gss_cred_id_t?, gss_name_t?, gss_OID?, gss_cred_usage_t, OM_uint32, OM_uint32, UnsafeMutablePointer<gss_cred_id_t?>, UnsafeMutablePointer<gss_OID_set?>?, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<OM_uint32>?) -> OM_uint32](/documentation/gss/gss_add_cred(_:_:_:_:_:_:_:_:_:_:_:))
- [func gss_set_cred_option(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_cred_id_t?>?, gss_OID, gss_buffer_t?) -> OM_uint32](/documentation/gss/gss_set_cred_option(_:_:_:_:))
- [func gss_release_cred(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_cred_id_t?>) -> OM_uint32](/documentation/gss/gss_release_cred(_:_:))
- [func gss_destroy_cred(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_cred_id_t?>) -> OM_uint32](/documentation/gss/gss_destroy_cred(_:_:))

### Initial Credential Keys

- [var kGSSICPassword: String](/documentation/gss/kgssicpassword)
- [var kGSSICCertificate: String](/documentation/gss/kgssiccertificate)
- [var kGSSCredentialUsage: String](/documentation/gss/kgsscredentialusage)
- [var kGSSICVerifyCredential: String](/documentation/gss/kgssicverifycredential)
- [var kGSSICLKDCHostname: String](/documentation/gss/kgssiclkdchostname)
- [var kGSSICKerberosCacheName: String](/documentation/gss/kgssickerberoscachename)
- [var kGSSICSiteName: String](/documentation/gss/kgssicsitename)
- [var kGSSICAppIdentifierACL: String](/documentation/gss/kgssicappidentifieracl)
- [var kGSSICCreateNewCredential: String](/documentation/gss/kgssiccreatenewcredential)
- [var kGSSICAppleSourceApp: String](/documentation/gss/kgssicapplesourceapp)
- [var kGSSICVerifyCredentialAcceptorName: String](/documentation/gss/kgssicverifycredentialacceptorname)
- [var kGSSICAuthenticationContext: String](/documentation/gss/kgssicauthenticationcontext)

### Pseudo Random Constants

- [var GSS_C_PRF_KEY_FULL: Int32](/documentation/gss/gss_c_prf_key_full)
- [var GSS_C_PRF_KEY_PARTIAL: Int32](/documentation/gss/gss_c_prf_key_partial)

### Credential Usage Values

- [var kGSS_C_INITIATE: String](/documentation/gss/kgss_c_initiate)
- [var kGSS_C_ACCEPT: String](/documentation/gss/kgss_c_accept)
- [var kGSS_C_BOTH: String](/documentation/gss/kgss_c_both)

### Password Keys

- [var kGSSChangePasswordOldPassword: String](/documentation/gss/kgsschangepasswordoldpassword)
- [var kGSSChangePasswordNewPassword: String](/documentation/gss/kgsschangepasswordnewpassword)

### Credential Masks and Macros

- [var GSS_C_INDEFINITE: UInt](/documentation/gss/gss_c_indefinite)
- [var GSS_C_INITIATE: Int32](/documentation/gss/gss_c_initiate)
- [var GSS_C_ACCEPT: Int32](/documentation/gss/gss_c_accept)
- [var GSS_C_BOTH: Int32](/documentation/gss/gss_c_both)
- [var GSS_C_OPTION_MASK: Int32](/documentation/gss/gss_c_option_mask)
- [var GSS_C_CRED_NO_UI: Int32](/documentation/gss/gss_c_cred_no_ui)
- [gss_auth_identity_t](/documentation/gss/gss_auth_identity_t)
- [gss_const_cred_id_t](/documentation/gss/gss_const_cred_id_t)
- [gss_cred_id_t](/documentation/gss/gss_cred_id_t)
- [gss_cred_usage_t](/documentation/gss/gss_cred_usage_t)

### Acquisition

- [func gss_aapl_initial_cred(gss_name_t, gss_const_OID, CFDictionary?, UnsafeMutablePointer<gss_cred_id_t?>, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> OM_uint32](/documentation/gss/gss_aapl_initial_cred(_:_:_:_:_:))
- [func gss_acquire_cred(UnsafeMutablePointer<OM_uint32>, gss_name_t?, OM_uint32, gss_OID_set?, gss_cred_usage_t, UnsafeMutablePointer<gss_cred_id_t?>, UnsafeMutablePointer<gss_OID_set?>?, UnsafeMutablePointer<OM_uint32>?) -> OM_uint32](/documentation/gss/gss_acquire_cred(_:_:_:_:_:_:_:_:))
- [func gss_acquire_cred_with_password(UnsafeMutablePointer<OM_uint32>, gss_name_t, gss_buffer_t, OM_uint32, gss_OID_set?, gss_cred_usage_t, UnsafeMutablePointer<gss_cred_id_t?>, UnsafeMutablePointer<gss_OID_set?>?, UnsafeMutablePointer<OM_uint32>?) -> OM_uint32](/documentation/gss/gss_acquire_cred_with_password(_:_:_:_:_:_:_:_:_:))
- [func GSSCredentialCopyUUID(gss_cred_id_t) -> Unmanaged<CFUUID>?](/documentation/gss/gsscredentialcopyuuid(_:))
- [func GSSCredentialCopyName(gss_cred_id_t) -> gss_name_t?](/documentation/gss/gsscredentialcopyname(_:))
- [func gss_pseudo_random(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, Int32, gss_buffer_t, Int, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_pseudo_random(_:_:_:_:_:_:))

### Inquiries

- [func gss_inquire_cred(UnsafeMutablePointer<OM_uint32>, gss_cred_id_t?, UnsafeMutablePointer<gss_name_t?>?, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<gss_cred_usage_t>?, UnsafeMutablePointer<gss_OID_set?>?) -> OM_uint32](/documentation/gss/gss_inquire_cred(_:_:_:_:_:_:))
- [func gss_inquire_cred_by_mech(UnsafeMutablePointer<OM_uint32>, gss_cred_id_t?, gss_OID, UnsafeMutablePointer<gss_name_t?>?, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<OM_uint32>?, UnsafeMutablePointer<gss_cred_usage_t>?) -> OM_uint32](/documentation/gss/gss_inquire_cred_by_mech(_:_:_:_:_:_:_:))
- [func gss_inquire_cred_by_oid(UnsafeMutablePointer<OM_uint32>, gss_cred_id_t, gss_OID, UnsafeMutablePointer<gss_buffer_set_t?>) -> OM_uint32](/documentation/gss/gss_inquire_cred_by_oid(_:_:_:_:))
- [func GSSCredentialGetLifetime(gss_cred_id_t) -> OM_uint32](/documentation/gss/gsscredentialgetlifetime(_:))

### Iteration

- [func gss_iter_creds(UnsafeMutablePointer<OM_uint32>, OM_uint32, gss_const_OID?, (gss_OID?, gss_cred_id_t?) -> Void) -> OM_uint32](/documentation/gss/gss_iter_creds(_:_:_:_:))
- [func gss_iter_creds_f(UnsafeMutablePointer<OM_uint32>, OM_uint32, gss_const_OID?, UnsafeMutableRawPointer?, (UnsafeMutableRawPointer?, gss_OID?, gss_cred_id_t?) -> Void) -> OM_uint32](/documentation/gss/gss_iter_creds_f(_:_:_:_:_:))

### Import and Export

- [func gss_import_cred(UnsafeMutablePointer<OM_uint32>, gss_buffer_t, UnsafeMutablePointer<gss_cred_id_t?>) -> OM_uint32](/documentation/gss/gss_import_cred(_:_:_:))
- [func gss_export_cred(UnsafeMutablePointer<OM_uint32>, gss_cred_id_t, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_export_cred(_:_:_:))
- [Security Mechanisms](/documentation/gss/security-mechanisms)

### Queries

- [func gss_indicate_mechs(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_OID_set?>) -> OM_uint32](/documentation/gss/gss_indicate_mechs(_:_:))
- [func gss_indicate_mechs_by_attrs(UnsafeMutablePointer<OM_uint32>, gss_const_OID_set?, gss_const_OID_set?, gss_const_OID_set?, UnsafeMutablePointer<gss_OID_set?>) -> OM_uint32](/documentation/gss/gss_indicate_mechs_by_attrs(_:_:_:_:_:))
- [func gss_display_mech_attr(UnsafeMutablePointer<OM_uint32>, gss_const_OID, gss_buffer_t?, gss_buffer_t?, gss_buffer_t?) -> OM_uint32](/documentation/gss/gss_display_mech_attr(_:_:_:_:_:))
- [func gss_inquire_attrs_for_mech(UnsafeMutablePointer<OM_uint32>, gss_const_OID, UnsafeMutablePointer<gss_OID_set?>?, UnsafeMutablePointer<gss_OID_set?>?) -> OM_uint32](/documentation/gss/gss_inquire_attrs_for_mech(_:_:_:_:))
- [func gss_inquire_mech_for_saslname(UnsafeMutablePointer<OM_uint32>, gss_buffer_t?, UnsafeMutablePointer<gss_OID?>) -> OM_uint32](/documentation/gss/gss_inquire_mech_for_saslname(_:_:_:))
- [func gss_inquire_saslname_for_mech(UnsafeMutablePointer<OM_uint32>, gss_OID, gss_buffer_t?, gss_buffer_t?, gss_buffer_t?) -> OM_uint32](/documentation/gss/gss_inquire_saslname_for_mech(_:_:_:_:_:))

## Names and Object Identifiers

- [Name Handling](/documentation/gss/name-handling)

### Creation and Destruction

- [gss_name_t](/documentation/gss/gss_name_t)
- [gss_const_name_t](/documentation/gss/gss_const_name_t)
- [func gss_canonicalize_name(UnsafeMutablePointer<OM_uint32>, gss_name_t, gss_OID, UnsafeMutablePointer<gss_name_t?>) -> OM_uint32](/documentation/gss/gss_canonicalize_name(_:_:_:_:))
- [func GSSNameCreateDisplayString(gss_name_t) -> Unmanaged<CFString>?](/documentation/gss/gssnamecreatedisplaystring(_:))
- [func GSSCreateName(CFTypeRef, gss_const_OID, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> gss_name_t?](/documentation/gss/gsscreatename(_:_:_:))
- [func gss_release_name(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_name_t?>) -> OM_uint32](/documentation/gss/gss_release_name(_:_:))

### Inquiries

- [func gss_display_name(UnsafeMutablePointer<OM_uint32>, gss_name_t, gss_buffer_t, UnsafeMutablePointer<gss_OID?>?) -> OM_uint32](/documentation/gss/gss_display_name(_:_:_:_:))
- [func gss_compare_name(UnsafeMutablePointer<OM_uint32>, gss_name_t, gss_name_t, UnsafeMutablePointer<Int32>) -> OM_uint32](/documentation/gss/gss_compare_name(_:_:_:_:))
- [func gss_inquire_name(UnsafeMutablePointer<OM_uint32>, gss_name_t, UnsafeMutablePointer<Int32>, UnsafeMutablePointer<gss_OID?>?, UnsafeMutablePointer<gss_buffer_set_t?>?) -> OM_uint32](/documentation/gss/gss_inquire_name(_:_:_:_:_:))
- [func gss_inquire_mechs_for_name(UnsafeMutablePointer<OM_uint32>, gss_name_t, UnsafeMutablePointer<gss_OID_set?>) -> OM_uint32](/documentation/gss/gss_inquire_mechs_for_name(_:_:_:))
- [func gss_inquire_names_for_mech(UnsafeMutablePointer<OM_uint32>, gss_const_OID, UnsafeMutablePointer<gss_OID_set?>) -> OM_uint32](/documentation/gss/gss_inquire_names_for_mech(_:_:_:))
- [func gss_duplicate_name(UnsafeMutablePointer<OM_uint32>, gss_name_t, UnsafeMutablePointer<gss_name_t?>) -> OM_uint32](/documentation/gss/gss_duplicate_name(_:_:_:))
- [func gss_aapl_change_password(gss_name_t, gss_const_OID, CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> OM_uint32](/documentation/gss/gss_aapl_change_password(_:_:_:_:))
- [func gss_userok(gss_name_t, UnsafePointer<CChar>) -> Int32](/documentation/gss/gss_userok(_:_:))

### Imports and Exports

- [func gss_export_name(UnsafeMutablePointer<OM_uint32>, gss_name_t, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_export_name(_:_:_:))
- [func gss_import_name(UnsafeMutablePointer<OM_uint32>, gss_buffer_t, gss_const_OID?, UnsafeMutablePointer<gss_name_t?>) -> OM_uint32](/documentation/gss/gss_import_name(_:_:_:_:))
- [Object Identifiers](/documentation/gss/object-identifiers)

### Object IDs

- [gss_OID](/documentation/gss/gss_oid)
- [gss_OID_set](/documentation/gss/gss_oid_set)
- [gss_OID_desc](/documentation/gss/gss_oid_desc)

#### Instance Properties

- [var elements: UnsafeMutableRawPointer!](/documentation/gss/gss_oid_desc_struct/elements)
- [var length: OM_uint32](/documentation/gss/gss_oid_desc_struct/length)
- [gss_const_OID](/documentation/gss/gss_const_oid)
- [gss_const_OID_set](/documentation/gss/gss_const_oid_set)
- [gss_OID_desc_struct](/documentation/gss/gss_oid_desc_struct)

#### Instance Properties

- [var elements: UnsafeMutableRawPointer!](/documentation/gss/gss_oid_desc_struct/elements)
- [var length: OM_uint32](/documentation/gss/gss_oid_desc_struct/length)

#### Initialization

- [init()](/documentation/gss/gss_oid_desc_struct/init())
- [init(length: OM_uint32, elements: UnsafeMutableRawPointer!)](/documentation/gss/gss_oid_desc_struct/init(length:elements:))
- [gss_OID_set_desc](/documentation/gss/gss_oid_set_desc)

#### Instance Properties

- [var count: Int](/documentation/gss/gss_oid_set_desc_struct/count)
- [var elements: gss_OID!](/documentation/gss/gss_oid_set_desc_struct/elements)
- [gss_OID_set_desc_struct](/documentation/gss/gss_oid_set_desc_struct)

#### Instance Properties

- [var count: Int](/documentation/gss/gss_oid_set_desc_struct/count)
- [var elements: gss_OID!](/documentation/gss/gss_oid_set_desc_struct/elements)

#### Initialization

- [init()](/documentation/gss/gss_oid_set_desc_struct/init())
- [init(count: Int, elements: gss_OID!)](/documentation/gss/gss_oid_set_desc_struct/init(count:elements:))

### Quality of Protection Constants

- [var GSS_C_QOP_DEFAULT: Int32](/documentation/gss/gss_c_qop_default)
- [var GSS_KRB5_CONF_C_QOP_DES: Int32](/documentation/gss/gss_krb5_conf_c_qop_des)
- [var GSS_KRB5_CONF_C_QOP_DES3_KD: Int32](/documentation/gss/gss_krb5_conf_c_qop_des3_kd)

### Creation and Release

- [func gss_create_empty_oid_set(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_OID_set?>) -> OM_uint32](/documentation/gss/gss_create_empty_oid_set(_:_:))
- [func gss_add_oid_set_member(UnsafeMutablePointer<OM_uint32>, gss_const_OID, UnsafeMutablePointer<gss_OID_set>) -> OM_uint32](/documentation/gss/gss_add_oid_set_member(_:_:_:))
- [func gss_release_oid_set(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_OID_set?>) -> OM_uint32](/documentation/gss/gss_release_oid_set(_:_:))
- [func gss_release_oid(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_OID?>) -> OM_uint32](/documentation/gss/gss_release_oid(_:_:))

### Conversion and Duplication

- [func gss_oid_to_str(UnsafeMutablePointer<OM_uint32>, gss_OID, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_oid_to_str(_:_:_:))
- [func gss_test_oid_set_member(UnsafeMutablePointer<OM_uint32>, gss_const_OID, gss_OID_set, UnsafeMutablePointer<Int32>) -> OM_uint32](/documentation/gss/gss_test_oid_set_member(_:_:_:_:))
- [func gss_oid_equal(gss_const_OID?, gss_const_OID?) -> Int32](/documentation/gss/gss_oid_equal(_:_:))
- [func gss_duplicate_oid(UnsafeMutablePointer<OM_uint32>, gss_OID, UnsafeMutablePointer<gss_OID?>) -> OM_uint32](/documentation/gss/gss_duplicate_oid(_:_:_:))

## Messages

- [Token Management](/documentation/gss/token-management)

### Buffer Flags

- [var GSS_IOV_BUFFER_FLAG_ALLOCATE: Int32](/documentation/gss/gss_iov_buffer_flag_allocate)
- [var GSS_IOV_BUFFER_FLAG_ALLOCATED: Int32](/documentation/gss/gss_iov_buffer_flag_allocated)
- [var GSS_IOV_BUFFER_TYPE_DATA: Int32](/documentation/gss/gss_iov_buffer_type_data)
- [var GSS_IOV_BUFFER_TYPE_EMPTY: Int32](/documentation/gss/gss_iov_buffer_type_empty)
- [var GSS_IOV_BUFFER_TYPE_FLAG_ALLOCATE: Int32](/documentation/gss/gss_iov_buffer_type_flag_allocate)
- [var GSS_IOV_BUFFER_TYPE_FLAG_ALLOCATED: Int32](/documentation/gss/gss_iov_buffer_type_flag_allocated)
- [var GSS_IOV_BUFFER_TYPE_FLAG_MASK: UInt32](/documentation/gss/gss_iov_buffer_type_flag_mask)
- [var GSS_IOV_BUFFER_TYPE_HEADER: Int32](/documentation/gss/gss_iov_buffer_type_header)
- [var GSS_IOV_BUFFER_TYPE_MECH_PARAMS: Int32](/documentation/gss/gss_iov_buffer_type_mech_params)
- [var GSS_IOV_BUFFER_TYPE_PADDING: Int32](/documentation/gss/gss_iov_buffer_type_padding)
- [var GSS_IOV_BUFFER_TYPE_SIGN_ONLY: Int32](/documentation/gss/gss_iov_buffer_type_sign_only)
- [var GSS_IOV_BUFFER_TYPE_STREAM: Int32](/documentation/gss/gss_iov_buffer_type_stream)
- [var GSS_IOV_BUFFER_TYPE_TRAILER: Int32](/documentation/gss/gss_iov_buffer_type_trailer)

### Encapsulation and Decapsulation

- [func gss_encapsulate_token(gss_const_buffer_t, gss_const_OID, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_encapsulate_token(_:_:_:))
- [func gss_decapsulate_token(gss_const_buffer_t, gss_const_OID, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_decapsulate_token(_:_:_:))
- [Message Protection](/documentation/gss/message-protection)

### Message Wrapping and Verification

- [func gss_get_mic(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, gss_qop_t, gss_buffer_t, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_get_mic(_:_:_:_:_:))
- [func gss_verify_mic(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, gss_buffer_t, gss_buffer_t, UnsafeMutablePointer<gss_qop_t>?) -> OM_uint32](/documentation/gss/gss_verify_mic(_:_:_:_:_:))
- [func gss_wrap(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, Int32, gss_qop_t, gss_buffer_t, UnsafeMutablePointer<Int32>?, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_wrap(_:_:_:_:_:_:_:))
- [func gss_unwrap(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, gss_buffer_t, gss_buffer_t, UnsafeMutablePointer<Int32>?, UnsafeMutablePointer<gss_qop_t>?) -> OM_uint32](/documentation/gss/gss_unwrap(_:_:_:_:_:_:))
- [func gss_sign(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, Int32, gss_buffer_t, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_sign(_:_:_:_:_:))
- [func gss_verify(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, gss_buffer_t, gss_buffer_t, UnsafeMutablePointer<Int32>) -> OM_uint32](/documentation/gss/gss_verify(_:_:_:_:_:))
- [func gss_seal(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, Int32, Int32, gss_buffer_t, UnsafeMutablePointer<Int32>, gss_buffer_t) -> OM_uint32](/documentation/gss/gss_seal(_:_:_:_:_:_:_:))
- [func gss_unseal(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, gss_buffer_t, gss_buffer_t, UnsafeMutablePointer<Int32>, UnsafeMutablePointer<Int32>) -> OM_uint32](/documentation/gss/gss_unseal(_:_:_:_:_:_:))
- [Kerberos Implementation](/documentation/gss/kerberos-implementation)

### Contexts and Keys

- [gss_krb5_cfx_keydata_t](/documentation/gss/gss_krb5_cfx_keydata_t)

#### Key Properties

- [var acceptor_subkey: gss_krb5_lucid_key_t](/documentation/gss/gss_krb5_cfx_keydata/acceptor_subkey)
- [var ctx_key: gss_krb5_lucid_key_t](/documentation/gss/gss_krb5_cfx_keydata/ctx_key)
- [var have_acceptor_subkey: OM_uint32](/documentation/gss/gss_krb5_cfx_keydata/have_acceptor_subkey)
- [gss_krb5_lucid_context_v1_t](/documentation/gss/gss_krb5_lucid_context_v1_t)

#### Context Members

- [var cfx_kd: gss_krb5_cfx_keydata_t](/documentation/gss/gss_krb5_lucid_context_v1/cfx_kd)
- [var endtime: OM_uint32](/documentation/gss/gss_krb5_lucid_context_v1/endtime)
- [var initiate: OM_uint32](/documentation/gss/gss_krb5_lucid_context_v1/initiate)
- [var `protocol`: OM_uint32](/documentation/gss/gss_krb5_lucid_context_v1/protocol)
- [var recv_seq: OM_uint64](/documentation/gss/gss_krb5_lucid_context_v1/recv_seq)
- [var rfc1964_kd: gss_krb5_rfc1964_keydata_t](/documentation/gss/gss_krb5_lucid_context_v1/rfc1964_kd)
- [var send_seq: OM_uint64](/documentation/gss/gss_krb5_lucid_context_v1/send_seq)
- [var version: OM_uint32](/documentation/gss/gss_krb5_lucid_context_v1/version)
- [gss_krb5_lucid_context_version_t](/documentation/gss/gss_krb5_lucid_context_version_t)

#### Context Members

- [var version: OM_uint32](/documentation/gss/gss_krb5_lucid_context_version/version)
- [gss_krb5_lucid_key_t](/documentation/gss/gss_krb5_lucid_key_t)

#### Key Members

- [var data: UnsafeMutableRawPointer?](/documentation/gss/gss_krb5_lucid_key/data)
- [var length: OM_uint32](/documentation/gss/gss_krb5_lucid_key/length)
- [var type: OM_uint32](/documentation/gss/gss_krb5_lucid_key/type)
- [gss_krb5_rfc1964_keydata_t](/documentation/gss/gss_krb5_rfc1964_keydata_t)

#### Key Data Members

- [var ctx_key: gss_krb5_lucid_key_t](/documentation/gss/gss_krb5_rfc1964_keydata/ctx_key)
- [var seal_alg: OM_uint32](/documentation/gss/gss_krb5_rfc1964_keydata/seal_alg)
- [var sign_alg: OM_uint32](/documentation/gss/gss_krb5_rfc1964_keydata/sign_alg)

### Identity and Settings

- [func gss_krb5_export_lucid_sec_context(UnsafeMutablePointer<OM_uint32>, UnsafeMutablePointer<gss_ctx_id_t?>, OM_uint32, UnsafeMutablePointer<UnsafeMutableRawPointer>?) -> OM_uint32](/documentation/gss/gss_krb5_export_lucid_sec_context(_:_:_:_:))
- [func gsskrb5_extract_authz_data_from_sec_context(UnsafeMutablePointer<OM_uint32>, gss_ctx_id_t, Int32, gss_buffer_t) -> OM_uint32](/documentation/gss/gsskrb5_extract_authz_data_from_sec_context(_:_:_:_:))
- [func gss_krb5_ccache_name(UnsafeMutablePointer<OM_uint32>, UnsafePointer<CChar>?, UnsafeMutablePointer<UnsafePointer<CChar>?>?) -> OM_uint32](/documentation/gss/gss_krb5_ccache_name(_:_:_:))
- [func gss_krb5_free_lucid_sec_context(UnsafeMutablePointer<OM_uint32>, UnsafeMutableRawPointer) -> OM_uint32](/documentation/gss/gss_krb5_free_lucid_sec_context(_:_:))
- [func gss_krb5_set_allowable_enctypes(UnsafeMutablePointer<OM_uint32>, gss_cred_id_t, OM_uint32, UnsafeMutablePointer<Int32>) -> OM_uint32](/documentation/gss/gss_krb5_set_allowable_enctypes(_:_:_:_:))
- [func gsskrb5_register_acceptor_identity(UnsafePointer<CChar>) -> OM_uint32](/documentation/gss/gsskrb5_register_acceptor_identity(_:))
- [func krb5_gss_register_acceptor_identity(UnsafePointer<CChar>) -> OM_uint32](/documentation/gss/krb5_gss_register_acceptor_identity(_:))
- [func gss_krb5_copy_ccache(UnsafeMutablePointer<OM_uint32>, gss_cred_id_t, OpaquePointer) -> OM_uint32](/documentation/gss/gss_krb5_copy_ccache(_:_:_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
