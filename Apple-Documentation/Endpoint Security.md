# Endpoint Security Documentation

Source: https://sosumi.ai/documentation/endpointsecurity

---
title: Endpoint Security
source: https://developer.apple.com/documentation/endpointsecurity
timestamp: 2026-02-13T18:56:33.675Z
---

## Event Monitoring

- [Client](/documentation/endpointsecurity/client)

### Creating a Client

- [func es_new_client(UnsafeMutablePointer<OpaquePointer?>, es_handler_block_t) -> es_new_client_result_t](/documentation/endpointsecurity/es_new_client(_:_:))
- [es_handler_block_t](/documentation/endpointsecurity/es_handler_block_t)
- [es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_t)

#### Success

- [var ES_NEW_CLIENT_RESULT_SUCCESS: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_success)

#### Errors

- [var ES_NEW_CLIENT_RESULT_ERR_INTERNAL: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_internal)
- [var ES_NEW_CLIENT_RESULT_ERR_INVALID_ARGUMENT: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_invalid_argument)
- [var ES_NEW_CLIENT_RESULT_ERR_NOT_ENTITLED: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_not_entitled)
- [var ES_NEW_CLIENT_RESULT_ERR_NOT_PERMITTED: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_not_permitted)
- [var ES_NEW_CLIENT_RESULT_ERR_NOT_PRIVILEGED: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_not_privileged)
- [var ES_NEW_CLIENT_RESULT_ERR_TOO_MANY_CLIENTS: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_too_many_clients)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_new_client_result_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_new_client_result_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_new_client_result_t/rawvalue)

### Destroying a Client

- [func es_delete_client(OpaquePointer?) -> es_return_t](/documentation/endpointsecurity/es_delete_client(_:))

### Subscribing to Events

- [func es_subscribe(OpaquePointer, UnsafePointer<es_event_type_t>, UInt32) -> es_return_t](/documentation/endpointsecurity/es_subscribe(_:_:_:))
- [func es_subscriptions(OpaquePointer, UnsafeMutablePointer<Int>, UnsafeMutablePointer<UnsafeMutablePointer<es_event_type_t>>?) -> es_return_t](/documentation/endpointsecurity/es_subscriptions(_:_:_:))
- [func es_unsubscribe(OpaquePointer, UnsafePointer<es_event_type_t>, UInt32) -> es_return_t](/documentation/endpointsecurity/es_unsubscribe(_:_:_:))
- [es_event_type_t](/documentation/endpointsecurity/es_event_type_t)

#### Authorization Event Types

- [var ES_EVENT_TYPE_AUTH_CHDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_chdir)
- [var ES_EVENT_TYPE_AUTH_CHROOT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_chroot)
- [var ES_EVENT_TYPE_AUTH_CLONE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_clone)
- [var ES_EVENT_TYPE_AUTH_COPYFILE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_copyfile)
- [var ES_EVENT_TYPE_AUTH_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_create)
- [var ES_EVENT_TYPE_AUTH_DELETEEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_deleteextattr)
- [var ES_EVENT_TYPE_AUTH_EXCHANGEDATA: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_exchangedata)
- [var ES_EVENT_TYPE_AUTH_EXEC: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_exec)
- [var ES_EVENT_TYPE_AUTH_FCNTL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_fcntl)
- [var ES_EVENT_TYPE_AUTH_FILE_PROVIDER_MATERIALIZE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_file_provider_materialize)
- [var ES_EVENT_TYPE_AUTH_FILE_PROVIDER_UPDATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_file_provider_update)
- [var ES_EVENT_TYPE_AUTH_FSGETPATH: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_fsgetpath)
- [var ES_EVENT_TYPE_AUTH_GET_TASK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_get_task)
- [var ES_EVENT_TYPE_AUTH_GET_TASK_READ: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_get_task_read)
- [var ES_EVENT_TYPE_AUTH_GETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_getattrlist)
- [var ES_EVENT_TYPE_AUTH_GETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_getextattr)
- [var ES_EVENT_TYPE_AUTH_IOKIT_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_iokit_open)
- [var ES_EVENT_TYPE_AUTH_KEXTLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_kextload)
- [var ES_EVENT_TYPE_AUTH_LINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_link)
- [var ES_EVENT_TYPE_AUTH_LISTEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_listextattr)
- [var ES_EVENT_TYPE_AUTH_MMAP: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mmap)
- [var ES_EVENT_TYPE_AUTH_MOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mount)
- [var ES_EVENT_TYPE_AUTH_MPROTECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mprotect)
- [var ES_EVENT_TYPE_AUTH_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_open)
- [var ES_EVENT_TYPE_AUTH_PROC_CHECK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_proc_check)
- [var ES_EVENT_TYPE_AUTH_PROC_SUSPEND_RESUME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_proc_suspend_resume)
- [var ES_EVENT_TYPE_AUTH_READDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_readdir)
- [var ES_EVENT_TYPE_AUTH_READLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_readlink)
- [var ES_EVENT_TYPE_AUTH_REMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_remount)
- [var ES_EVENT_TYPE_AUTH_RENAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_rename)
- [var ES_EVENT_TYPE_AUTH_SEARCHFS: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_searchfs)
- [var ES_EVENT_TYPE_AUTH_SETACL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setacl)
- [var ES_EVENT_TYPE_AUTH_SETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setattrlist)
- [var ES_EVENT_TYPE_AUTH_SETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setextattr)
- [var ES_EVENT_TYPE_AUTH_SETFLAGS: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setflags)
- [var ES_EVENT_TYPE_AUTH_SETMODE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setmode)
- [var ES_EVENT_TYPE_AUTH_SETOWNER: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setowner)
- [var ES_EVENT_TYPE_AUTH_SETTIME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_settime)
- [var ES_EVENT_TYPE_AUTH_SIGNAL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_signal)
- [var ES_EVENT_TYPE_AUTH_TRUNCATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_truncate)
- [var ES_EVENT_TYPE_AUTH_UIPC_BIND: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_uipc_bind)
- [var ES_EVENT_TYPE_AUTH_UIPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_uipc_connect)
- [var ES_EVENT_TYPE_AUTH_UNLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_unlink)
- [var ES_EVENT_TYPE_AUTH_UTIMES: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_utimes)

#### Notification Event Types

- [var ES_EVENT_TYPE_NOTIFY_ACCESS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_access)
- [var ES_EVENT_TYPE_NOTIFY_CHDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_chdir)
- [var ES_EVENT_TYPE_NOTIFY_CHROOT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_chroot)
- [var ES_EVENT_TYPE_NOTIFY_CLONE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_clone)
- [var ES_EVENT_TYPE_NOTIFY_CLOSE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_close)
- [var ES_EVENT_TYPE_NOTIFY_COPYFILE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_copyfile)
- [var ES_EVENT_TYPE_NOTIFY_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_create)
- [var ES_EVENT_TYPE_NOTIFY_CS_INVALIDATED: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_cs_invalidated)
- [var ES_EVENT_TYPE_NOTIFY_DELETEEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_deleteextattr)
- [var ES_EVENT_TYPE_NOTIFY_DUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_dup)
- [var ES_EVENT_TYPE_NOTIFY_EXCHANGEDATA: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exchangedata)
- [var ES_EVENT_TYPE_NOTIFY_EXEC: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exec)
- [var ES_EVENT_TYPE_NOTIFY_EXIT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exit)
- [var ES_EVENT_TYPE_NOTIFY_FCNTL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fcntl)
- [var ES_EVENT_TYPE_NOTIFY_FILE_PROVIDER_MATERIALIZE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_file_provider_materialize)
- [var ES_EVENT_TYPE_NOTIFY_FILE_PROVIDER_UPDATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_file_provider_update)
- [var ES_EVENT_TYPE_NOTIFY_FORK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fork)
- [var ES_EVENT_TYPE_NOTIFY_FSGETPATH: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fsgetpath)
- [var ES_EVENT_TYPE_NOTIFY_GETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_getattrlist)
- [var ES_EVENT_TYPE_NOTIFY_GETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_getextattr)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_READ: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_read)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_INSPECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_inspect)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_NAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_name)
- [var ES_EVENT_TYPE_NOTIFY_IOKIT_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_iokit_open)
- [var ES_EVENT_TYPE_NOTIFY_KEXTLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_kextload)
- [var ES_EVENT_TYPE_NOTIFY_KEXTUNLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_kextunload)
- [var ES_EVENT_TYPE_NOTIFY_LINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_link)
- [var ES_EVENT_TYPE_NOTIFY_LISTEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_listextattr)
- [var ES_EVENT_TYPE_NOTIFY_LOOKUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_lookup)
- [var ES_EVENT_TYPE_NOTIFY_MMAP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mmap)
- [var ES_EVENT_TYPE_NOTIFY_MOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mount)
- [var ES_EVENT_TYPE_NOTIFY_MPROTECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mprotect)
- [var ES_EVENT_TYPE_NOTIFY_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_open)
- [var ES_EVENT_TYPE_NOTIFY_PROC_CHECK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_proc_check)
- [var ES_EVENT_TYPE_NOTIFY_PROC_SUSPEND_RESUME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_proc_suspend_resume)
- [var ES_EVENT_TYPE_NOTIFY_PTY_CLOSE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_pty_close)
- [var ES_EVENT_TYPE_NOTIFY_PTY_GRANT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_pty_grant)
- [var ES_EVENT_TYPE_NOTIFY_READDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_readdir)
- [var ES_EVENT_TYPE_NOTIFY_READLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_readlink)
- [var ES_EVENT_TYPE_NOTIFY_REMOTE_THREAD_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_remote_thread_create)
- [var ES_EVENT_TYPE_NOTIFY_REMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_remount)
- [var ES_EVENT_TYPE_NOTIFY_RENAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_rename)
- [var ES_EVENT_TYPE_NOTIFY_SEARCHFS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_searchfs)
- [var ES_EVENT_TYPE_NOTIFY_SETACL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setacl)
- [var ES_EVENT_TYPE_NOTIFY_SETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setattrlist)
- [var ES_EVENT_TYPE_NOTIFY_SETEGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setegid)
- [var ES_EVENT_TYPE_NOTIFY_SETEUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_seteuid)
- [var ES_EVENT_TYPE_NOTIFY_SETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setextattr)
- [var ES_EVENT_TYPE_NOTIFY_SETGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setgid)
- [var ES_EVENT_TYPE_NOTIFY_SETFLAGS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setflags)
- [var ES_EVENT_TYPE_NOTIFY_SETMODE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setmode)
- [var ES_EVENT_TYPE_NOTIFY_SETOWNER: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setowner)
- [var ES_EVENT_TYPE_NOTIFY_SETREGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setregid)
- [var ES_EVENT_TYPE_NOTIFY_SETREUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setreuid)
- [var ES_EVENT_TYPE_NOTIFY_SETTIME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_settime)
- [var ES_EVENT_TYPE_NOTIFY_SETUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setuid)
- [var ES_EVENT_TYPE_NOTIFY_SIGNAL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_signal)
- [var ES_EVENT_TYPE_NOTIFY_STAT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_stat)
- [var ES_EVENT_TYPE_NOTIFY_TRACE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_trace)
- [var ES_EVENT_TYPE_NOTIFY_TRUNCATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_truncate)
- [var ES_EVENT_TYPE_NOTIFY_UIPC_BIND: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_uipc_bind)
- [var ES_EVENT_TYPE_NOTIFY_UIPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_uipc_connect)
- [var ES_EVENT_TYPE_NOTIFY_UNLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_unlink)
- [var ES_EVENT_TYPE_NOTIFY_UNMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_unmount)
- [var ES_EVENT_TYPE_NOTIFY_UTIMES: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_utimes)
- [var ES_EVENT_TYPE_NOTIFY_WRITE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_write)

#### Enumeration Marker

- [var ES_EVENT_TYPE_LAST: es_event_type_t](/documentation/endpointsecurity/es_event_type_last)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_event_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_event_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_event_type_t/rawvalue)
- [func es_unsubscribe_all(OpaquePointer) -> es_return_t](/documentation/endpointsecurity/es_unsubscribe_all(_:))

### Responding to Events

- [func es_respond_auth_result(OpaquePointer, UnsafePointer<es_message_t>, es_auth_result_t, Bool) -> es_respond_result_t](/documentation/endpointsecurity/es_respond_auth_result(_:_:_:_:))
- [es_auth_result_t](/documentation/endpointsecurity/es_auth_result_t)

#### Authorization Values

- [var ES_AUTH_RESULT_ALLOW: es_auth_result_t](/documentation/endpointsecurity/es_auth_result_allow)
- [var ES_AUTH_RESULT_DENY: es_auth_result_t](/documentation/endpointsecurity/es_auth_result_deny)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_auth_result_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_auth_result_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_auth_result_t/rawvalue)
- [func es_respond_flags_result(OpaquePointer, UnsafePointer<es_message_t>, UInt32, Bool) -> es_respond_result_t](/documentation/endpointsecurity/es_respond_flags_result(_:_:_:_:))
- [es_respond_result_t](/documentation/endpointsecurity/es_respond_result_t)

#### Success

- [var ES_RESPOND_RESULT_SUCCESS: es_respond_result_t](/documentation/endpointsecurity/es_respond_result_success)

#### Errors

- [var ES_RESPOND_RESULT_ERR_DUPLICATE_RESPONSE: es_respond_result_t](/documentation/endpointsecurity/es_respond_result_err_duplicate_response)
- [var ES_RESPOND_RESULT_ERR_INTERNAL: es_respond_result_t](/documentation/endpointsecurity/es_respond_result_err_internal)
- [var ES_RESPOND_RESULT_ERR_INVALID_ARGUMENT: es_respond_result_t](/documentation/endpointsecurity/es_respond_result_err_invalid_argument)
- [var ES_RESPOND_RESULT_NOT_FOUND: es_respond_result_t](/documentation/endpointsecurity/es_respond_result_not_found)
- [var ES_RESPOND_RESULT_ERR_EVENT_TYPE: es_respond_result_t](/documentation/endpointsecurity/es_respond_result_err_event_type)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_respond_result_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_respond_result_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_respond_result_t/rawvalue)

### Managing Cached Results

- [func es_clear_cache(OpaquePointer) -> es_clear_cache_result_t](/documentation/endpointsecurity/es_clear_cache(_:))
- [es_clear_cache_result_t](/documentation/endpointsecurity/es_clear_cache_result_t)

#### Success

- [var ES_CLEAR_CACHE_RESULT_SUCCESS: es_clear_cache_result_t](/documentation/endpointsecurity/es_clear_cache_result_success)

#### Errors

- [var ES_CLEAR_CACHE_RESULT_ERR_INTERNAL: es_clear_cache_result_t](/documentation/endpointsecurity/es_clear_cache_result_err_internal)
- [var ES_CLEAR_CACHE_RESULT_ERR_THROTTLE: es_clear_cache_result_t](/documentation/endpointsecurity/es_clear_cache_result_err_throttle)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_clear_cache_result_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_clear_cache_result_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_clear_cache_result_t/rawvalue)

### Muting Events

- [func es_mute_process(OpaquePointer, UnsafePointer<audit_token_t>) -> es_return_t](/documentation/endpointsecurity/es_mute_process(_:_:))
- [func es_mute_process_events(OpaquePointer, UnsafePointer<audit_token_t>, UnsafePointer<es_event_type_t>, Int) -> es_return_t](/documentation/endpointsecurity/es_mute_process_events(_:_:_:_:))
- [es_muted_processes_t](/documentation/endpointsecurity/es_muted_processes_t)

#### Accessing Muted Processes

- [var processes: UnsafePointer<es_muted_process_t>!](/documentation/endpointsecurity/es_muted_processes_t/processes)
- [es_muted_process_t](/documentation/endpointsecurity/es_muted_process_t)

##### Accessing Muted Processes

- [var audit_token: audit_token_t](/documentation/endpointsecurity/es_muted_process_t/audit_token)
- [var events: UnsafePointer<es_event_type_t>!](/documentation/endpointsecurity/es_muted_process_t/events)
- [es_event_type_t](/documentation/endpointsecurity/es_event_type_t)

###### Authorization Event Types

- [var ES_EVENT_TYPE_AUTH_CHDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_chdir)
- [var ES_EVENT_TYPE_AUTH_CHROOT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_chroot)
- [var ES_EVENT_TYPE_AUTH_CLONE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_clone)
- [var ES_EVENT_TYPE_AUTH_COPYFILE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_copyfile)
- [var ES_EVENT_TYPE_AUTH_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_create)
- [var ES_EVENT_TYPE_AUTH_DELETEEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_deleteextattr)
- [var ES_EVENT_TYPE_AUTH_EXCHANGEDATA: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_exchangedata)
- [var ES_EVENT_TYPE_AUTH_EXEC: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_exec)
- [var ES_EVENT_TYPE_AUTH_FCNTL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_fcntl)
- [var ES_EVENT_TYPE_AUTH_FILE_PROVIDER_MATERIALIZE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_file_provider_materialize)
- [var ES_EVENT_TYPE_AUTH_FILE_PROVIDER_UPDATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_file_provider_update)
- [var ES_EVENT_TYPE_AUTH_FSGETPATH: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_fsgetpath)
- [var ES_EVENT_TYPE_AUTH_GET_TASK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_get_task)
- [var ES_EVENT_TYPE_AUTH_GET_TASK_READ: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_get_task_read)
- [var ES_EVENT_TYPE_AUTH_GETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_getattrlist)
- [var ES_EVENT_TYPE_AUTH_GETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_getextattr)
- [var ES_EVENT_TYPE_AUTH_IOKIT_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_iokit_open)
- [var ES_EVENT_TYPE_AUTH_KEXTLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_kextload)
- [var ES_EVENT_TYPE_AUTH_LINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_link)
- [var ES_EVENT_TYPE_AUTH_LISTEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_listextattr)
- [var ES_EVENT_TYPE_AUTH_MMAP: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mmap)
- [var ES_EVENT_TYPE_AUTH_MOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mount)
- [var ES_EVENT_TYPE_AUTH_MPROTECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mprotect)
- [var ES_EVENT_TYPE_AUTH_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_open)
- [var ES_EVENT_TYPE_AUTH_PROC_CHECK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_proc_check)
- [var ES_EVENT_TYPE_AUTH_PROC_SUSPEND_RESUME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_proc_suspend_resume)
- [var ES_EVENT_TYPE_AUTH_READDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_readdir)
- [var ES_EVENT_TYPE_AUTH_READLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_readlink)
- [var ES_EVENT_TYPE_AUTH_REMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_remount)
- [var ES_EVENT_TYPE_AUTH_RENAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_rename)
- [var ES_EVENT_TYPE_AUTH_SEARCHFS: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_searchfs)
- [var ES_EVENT_TYPE_AUTH_SETACL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setacl)
- [var ES_EVENT_TYPE_AUTH_SETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setattrlist)
- [var ES_EVENT_TYPE_AUTH_SETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setextattr)
- [var ES_EVENT_TYPE_AUTH_SETFLAGS: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setflags)
- [var ES_EVENT_TYPE_AUTH_SETMODE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setmode)
- [var ES_EVENT_TYPE_AUTH_SETOWNER: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setowner)
- [var ES_EVENT_TYPE_AUTH_SETTIME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_settime)
- [var ES_EVENT_TYPE_AUTH_SIGNAL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_signal)
- [var ES_EVENT_TYPE_AUTH_TRUNCATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_truncate)
- [var ES_EVENT_TYPE_AUTH_UIPC_BIND: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_uipc_bind)
- [var ES_EVENT_TYPE_AUTH_UIPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_uipc_connect)
- [var ES_EVENT_TYPE_AUTH_UNLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_unlink)
- [var ES_EVENT_TYPE_AUTH_UTIMES: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_utimes)

###### Notification Event Types

- [var ES_EVENT_TYPE_NOTIFY_ACCESS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_access)
- [var ES_EVENT_TYPE_NOTIFY_CHDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_chdir)
- [var ES_EVENT_TYPE_NOTIFY_CHROOT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_chroot)
- [var ES_EVENT_TYPE_NOTIFY_CLONE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_clone)
- [var ES_EVENT_TYPE_NOTIFY_CLOSE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_close)
- [var ES_EVENT_TYPE_NOTIFY_COPYFILE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_copyfile)
- [var ES_EVENT_TYPE_NOTIFY_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_create)
- [var ES_EVENT_TYPE_NOTIFY_CS_INVALIDATED: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_cs_invalidated)
- [var ES_EVENT_TYPE_NOTIFY_DELETEEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_deleteextattr)
- [var ES_EVENT_TYPE_NOTIFY_DUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_dup)
- [var ES_EVENT_TYPE_NOTIFY_EXCHANGEDATA: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exchangedata)
- [var ES_EVENT_TYPE_NOTIFY_EXEC: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exec)
- [var ES_EVENT_TYPE_NOTIFY_EXIT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exit)
- [var ES_EVENT_TYPE_NOTIFY_FCNTL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fcntl)
- [var ES_EVENT_TYPE_NOTIFY_FILE_PROVIDER_MATERIALIZE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_file_provider_materialize)
- [var ES_EVENT_TYPE_NOTIFY_FILE_PROVIDER_UPDATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_file_provider_update)
- [var ES_EVENT_TYPE_NOTIFY_FORK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fork)
- [var ES_EVENT_TYPE_NOTIFY_FSGETPATH: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fsgetpath)
- [var ES_EVENT_TYPE_NOTIFY_GETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_getattrlist)
- [var ES_EVENT_TYPE_NOTIFY_GETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_getextattr)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_READ: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_read)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_INSPECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_inspect)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_NAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_name)
- [var ES_EVENT_TYPE_NOTIFY_IOKIT_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_iokit_open)
- [var ES_EVENT_TYPE_NOTIFY_KEXTLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_kextload)
- [var ES_EVENT_TYPE_NOTIFY_KEXTUNLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_kextunload)
- [var ES_EVENT_TYPE_NOTIFY_LINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_link)
- [var ES_EVENT_TYPE_NOTIFY_LISTEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_listextattr)
- [var ES_EVENT_TYPE_NOTIFY_LOOKUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_lookup)
- [var ES_EVENT_TYPE_NOTIFY_MMAP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mmap)
- [var ES_EVENT_TYPE_NOTIFY_MOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mount)
- [var ES_EVENT_TYPE_NOTIFY_MPROTECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mprotect)
- [var ES_EVENT_TYPE_NOTIFY_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_open)
- [var ES_EVENT_TYPE_NOTIFY_PROC_CHECK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_proc_check)
- [var ES_EVENT_TYPE_NOTIFY_PROC_SUSPEND_RESUME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_proc_suspend_resume)
- [var ES_EVENT_TYPE_NOTIFY_PTY_CLOSE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_pty_close)
- [var ES_EVENT_TYPE_NOTIFY_PTY_GRANT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_pty_grant)
- [var ES_EVENT_TYPE_NOTIFY_READDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_readdir)
- [var ES_EVENT_TYPE_NOTIFY_READLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_readlink)
- [var ES_EVENT_TYPE_NOTIFY_REMOTE_THREAD_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_remote_thread_create)
- [var ES_EVENT_TYPE_NOTIFY_REMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_remount)
- [var ES_EVENT_TYPE_NOTIFY_RENAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_rename)
- [var ES_EVENT_TYPE_NOTIFY_SEARCHFS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_searchfs)
- [var ES_EVENT_TYPE_NOTIFY_SETACL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setacl)
- [var ES_EVENT_TYPE_NOTIFY_SETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setattrlist)
- [var ES_EVENT_TYPE_NOTIFY_SETEGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setegid)
- [var ES_EVENT_TYPE_NOTIFY_SETEUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_seteuid)
- [var ES_EVENT_TYPE_NOTIFY_SETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setextattr)
- [var ES_EVENT_TYPE_NOTIFY_SETGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setgid)
- [var ES_EVENT_TYPE_NOTIFY_SETFLAGS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setflags)
- [var ES_EVENT_TYPE_NOTIFY_SETMODE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setmode)
- [var ES_EVENT_TYPE_NOTIFY_SETOWNER: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setowner)
- [var ES_EVENT_TYPE_NOTIFY_SETREGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setregid)
- [var ES_EVENT_TYPE_NOTIFY_SETREUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setreuid)
- [var ES_EVENT_TYPE_NOTIFY_SETTIME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_settime)
- [var ES_EVENT_TYPE_NOTIFY_SETUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setuid)
- [var ES_EVENT_TYPE_NOTIFY_SIGNAL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_signal)
- [var ES_EVENT_TYPE_NOTIFY_STAT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_stat)
- [var ES_EVENT_TYPE_NOTIFY_TRACE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_trace)
- [var ES_EVENT_TYPE_NOTIFY_TRUNCATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_truncate)
- [var ES_EVENT_TYPE_NOTIFY_UIPC_BIND: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_uipc_bind)
- [var ES_EVENT_TYPE_NOTIFY_UIPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_uipc_connect)
- [var ES_EVENT_TYPE_NOTIFY_UNLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_unlink)
- [var ES_EVENT_TYPE_NOTIFY_UNMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_unmount)
- [var ES_EVENT_TYPE_NOTIFY_UTIMES: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_utimes)
- [var ES_EVENT_TYPE_NOTIFY_WRITE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_write)

###### Enumeration Marker

- [var ES_EVENT_TYPE_LAST: es_event_type_t](/documentation/endpointsecurity/es_event_type_last)

###### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_event_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_event_type_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_event_type_t/rawvalue)
- [var event_count: Int](/documentation/endpointsecurity/es_muted_process_t/event_count)

##### Initializers

- [init()](/documentation/endpointsecurity/es_muted_process_t/init())
- [init(audit_token: audit_token_t, event_count: Int, events: UnsafePointer<es_event_type_t>!)](/documentation/endpointsecurity/es_muted_process_t/init(audit_token:event_count:events:))
- [var count: Int](/documentation/endpointsecurity/es_muted_processes_t/count)

#### Initializers

- [init()](/documentation/endpointsecurity/es_muted_processes_t/init())
- [init(count: Int, processes: UnsafePointer<es_muted_process_t>!)](/documentation/endpointsecurity/es_muted_processes_t/init(count:processes:))
- [func es_release_muted_processes(UnsafeMutablePointer<es_muted_processes_t>)](/documentation/endpointsecurity/es_release_muted_processes(_:))
- [func es_muted_processes_events(OpaquePointer, UnsafeMutablePointer<UnsafeMutablePointer<es_muted_processes_t>?>) -> es_return_t](/documentation/endpointsecurity/es_muted_processes_events(_:_:))
- [func es_mute_path(OpaquePointer, UnsafePointer<CChar>, es_mute_path_type_t) -> es_return_t](/documentation/endpointsecurity/es_mute_path(_:_:_:))
- [func es_mute_path_events(OpaquePointer, UnsafePointer<CChar>, es_mute_path_type_t, UnsafePointer<es_event_type_t>, Int) -> es_return_t](/documentation/endpointsecurity/es_mute_path_events(_:_:_:_:_:))
- [es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_t)

#### Path Types

- [var ES_MUTE_PATH_TYPE_PREFIX: es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_prefix)
- [var ES_MUTE_PATH_TYPE_LITERAL: es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_literal)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_mute_path_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_mute_path_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_mute_path_type_t/rawvalue)
- [func es_muted_paths_events(OpaquePointer, UnsafeMutablePointer<UnsafeMutablePointer<es_muted_paths_t>>?) -> es_return_t](/documentation/endpointsecurity/es_muted_paths_events(_:_:))
- [es_muted_paths_t](/documentation/endpointsecurity/es_muted_paths_t)

#### Accessing Muted Paths

- [var paths: UnsafePointer<es_muted_path_t>!](/documentation/endpointsecurity/es_muted_paths_t/paths)
- [es_muted_path_t](/documentation/endpointsecurity/es_muted_path_t)

##### Accessing Muted Path Properties

- [var type: es_mute_path_type_t](/documentation/endpointsecurity/es_muted_path_t/type)
- [es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_t)

###### Path Types

- [var ES_MUTE_PATH_TYPE_PREFIX: es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_prefix)
- [var ES_MUTE_PATH_TYPE_LITERAL: es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_literal)

###### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_mute_path_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_mute_path_type_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_mute_path_type_t/rawvalue)
- [var events: UnsafePointer<es_event_type_t>!](/documentation/endpointsecurity/es_muted_path_t/events)
- [es_event_type_t](/documentation/endpointsecurity/es_event_type_t)

###### Authorization Event Types

- [var ES_EVENT_TYPE_AUTH_CHDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_chdir)
- [var ES_EVENT_TYPE_AUTH_CHROOT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_chroot)
- [var ES_EVENT_TYPE_AUTH_CLONE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_clone)
- [var ES_EVENT_TYPE_AUTH_COPYFILE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_copyfile)
- [var ES_EVENT_TYPE_AUTH_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_create)
- [var ES_EVENT_TYPE_AUTH_DELETEEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_deleteextattr)
- [var ES_EVENT_TYPE_AUTH_EXCHANGEDATA: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_exchangedata)
- [var ES_EVENT_TYPE_AUTH_EXEC: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_exec)
- [var ES_EVENT_TYPE_AUTH_FCNTL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_fcntl)
- [var ES_EVENT_TYPE_AUTH_FILE_PROVIDER_MATERIALIZE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_file_provider_materialize)
- [var ES_EVENT_TYPE_AUTH_FILE_PROVIDER_UPDATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_file_provider_update)
- [var ES_EVENT_TYPE_AUTH_FSGETPATH: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_fsgetpath)
- [var ES_EVENT_TYPE_AUTH_GET_TASK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_get_task)
- [var ES_EVENT_TYPE_AUTH_GET_TASK_READ: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_get_task_read)
- [var ES_EVENT_TYPE_AUTH_GETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_getattrlist)
- [var ES_EVENT_TYPE_AUTH_GETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_getextattr)
- [var ES_EVENT_TYPE_AUTH_IOKIT_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_iokit_open)
- [var ES_EVENT_TYPE_AUTH_KEXTLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_kextload)
- [var ES_EVENT_TYPE_AUTH_LINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_link)
- [var ES_EVENT_TYPE_AUTH_LISTEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_listextattr)
- [var ES_EVENT_TYPE_AUTH_MMAP: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mmap)
- [var ES_EVENT_TYPE_AUTH_MOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mount)
- [var ES_EVENT_TYPE_AUTH_MPROTECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mprotect)
- [var ES_EVENT_TYPE_AUTH_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_open)
- [var ES_EVENT_TYPE_AUTH_PROC_CHECK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_proc_check)
- [var ES_EVENT_TYPE_AUTH_PROC_SUSPEND_RESUME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_proc_suspend_resume)
- [var ES_EVENT_TYPE_AUTH_READDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_readdir)
- [var ES_EVENT_TYPE_AUTH_READLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_readlink)
- [var ES_EVENT_TYPE_AUTH_REMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_remount)
- [var ES_EVENT_TYPE_AUTH_RENAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_rename)
- [var ES_EVENT_TYPE_AUTH_SEARCHFS: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_searchfs)
- [var ES_EVENT_TYPE_AUTH_SETACL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setacl)
- [var ES_EVENT_TYPE_AUTH_SETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setattrlist)
- [var ES_EVENT_TYPE_AUTH_SETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setextattr)
- [var ES_EVENT_TYPE_AUTH_SETFLAGS: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setflags)
- [var ES_EVENT_TYPE_AUTH_SETMODE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setmode)
- [var ES_EVENT_TYPE_AUTH_SETOWNER: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setowner)
- [var ES_EVENT_TYPE_AUTH_SETTIME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_settime)
- [var ES_EVENT_TYPE_AUTH_SIGNAL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_signal)
- [var ES_EVENT_TYPE_AUTH_TRUNCATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_truncate)
- [var ES_EVENT_TYPE_AUTH_UIPC_BIND: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_uipc_bind)
- [var ES_EVENT_TYPE_AUTH_UIPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_uipc_connect)
- [var ES_EVENT_TYPE_AUTH_UNLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_unlink)
- [var ES_EVENT_TYPE_AUTH_UTIMES: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_utimes)

###### Notification Event Types

- [var ES_EVENT_TYPE_NOTIFY_ACCESS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_access)
- [var ES_EVENT_TYPE_NOTIFY_CHDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_chdir)
- [var ES_EVENT_TYPE_NOTIFY_CHROOT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_chroot)
- [var ES_EVENT_TYPE_NOTIFY_CLONE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_clone)
- [var ES_EVENT_TYPE_NOTIFY_CLOSE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_close)
- [var ES_EVENT_TYPE_NOTIFY_COPYFILE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_copyfile)
- [var ES_EVENT_TYPE_NOTIFY_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_create)
- [var ES_EVENT_TYPE_NOTIFY_CS_INVALIDATED: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_cs_invalidated)
- [var ES_EVENT_TYPE_NOTIFY_DELETEEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_deleteextattr)
- [var ES_EVENT_TYPE_NOTIFY_DUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_dup)
- [var ES_EVENT_TYPE_NOTIFY_EXCHANGEDATA: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exchangedata)
- [var ES_EVENT_TYPE_NOTIFY_EXEC: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exec)
- [var ES_EVENT_TYPE_NOTIFY_EXIT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exit)
- [var ES_EVENT_TYPE_NOTIFY_FCNTL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fcntl)
- [var ES_EVENT_TYPE_NOTIFY_FILE_PROVIDER_MATERIALIZE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_file_provider_materialize)
- [var ES_EVENT_TYPE_NOTIFY_FILE_PROVIDER_UPDATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_file_provider_update)
- [var ES_EVENT_TYPE_NOTIFY_FORK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fork)
- [var ES_EVENT_TYPE_NOTIFY_FSGETPATH: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fsgetpath)
- [var ES_EVENT_TYPE_NOTIFY_GETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_getattrlist)
- [var ES_EVENT_TYPE_NOTIFY_GETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_getextattr)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_READ: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_read)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_INSPECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_inspect)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_NAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_name)
- [var ES_EVENT_TYPE_NOTIFY_IOKIT_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_iokit_open)
- [var ES_EVENT_TYPE_NOTIFY_KEXTLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_kextload)
- [var ES_EVENT_TYPE_NOTIFY_KEXTUNLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_kextunload)
- [var ES_EVENT_TYPE_NOTIFY_LINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_link)
- [var ES_EVENT_TYPE_NOTIFY_LISTEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_listextattr)
- [var ES_EVENT_TYPE_NOTIFY_LOOKUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_lookup)
- [var ES_EVENT_TYPE_NOTIFY_MMAP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mmap)
- [var ES_EVENT_TYPE_NOTIFY_MOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mount)
- [var ES_EVENT_TYPE_NOTIFY_MPROTECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mprotect)
- [var ES_EVENT_TYPE_NOTIFY_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_open)
- [var ES_EVENT_TYPE_NOTIFY_PROC_CHECK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_proc_check)
- [var ES_EVENT_TYPE_NOTIFY_PROC_SUSPEND_RESUME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_proc_suspend_resume)
- [var ES_EVENT_TYPE_NOTIFY_PTY_CLOSE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_pty_close)
- [var ES_EVENT_TYPE_NOTIFY_PTY_GRANT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_pty_grant)
- [var ES_EVENT_TYPE_NOTIFY_READDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_readdir)
- [var ES_EVENT_TYPE_NOTIFY_READLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_readlink)
- [var ES_EVENT_TYPE_NOTIFY_REMOTE_THREAD_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_remote_thread_create)
- [var ES_EVENT_TYPE_NOTIFY_REMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_remount)
- [var ES_EVENT_TYPE_NOTIFY_RENAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_rename)
- [var ES_EVENT_TYPE_NOTIFY_SEARCHFS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_searchfs)
- [var ES_EVENT_TYPE_NOTIFY_SETACL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setacl)
- [var ES_EVENT_TYPE_NOTIFY_SETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setattrlist)
- [var ES_EVENT_TYPE_NOTIFY_SETEGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setegid)
- [var ES_EVENT_TYPE_NOTIFY_SETEUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_seteuid)
- [var ES_EVENT_TYPE_NOTIFY_SETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setextattr)
- [var ES_EVENT_TYPE_NOTIFY_SETGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setgid)
- [var ES_EVENT_TYPE_NOTIFY_SETFLAGS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setflags)
- [var ES_EVENT_TYPE_NOTIFY_SETMODE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setmode)
- [var ES_EVENT_TYPE_NOTIFY_SETOWNER: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setowner)
- [var ES_EVENT_TYPE_NOTIFY_SETREGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setregid)
- [var ES_EVENT_TYPE_NOTIFY_SETREUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setreuid)
- [var ES_EVENT_TYPE_NOTIFY_SETTIME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_settime)
- [var ES_EVENT_TYPE_NOTIFY_SETUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setuid)
- [var ES_EVENT_TYPE_NOTIFY_SIGNAL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_signal)
- [var ES_EVENT_TYPE_NOTIFY_STAT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_stat)
- [var ES_EVENT_TYPE_NOTIFY_TRACE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_trace)
- [var ES_EVENT_TYPE_NOTIFY_TRUNCATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_truncate)
- [var ES_EVENT_TYPE_NOTIFY_UIPC_BIND: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_uipc_bind)
- [var ES_EVENT_TYPE_NOTIFY_UIPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_uipc_connect)
- [var ES_EVENT_TYPE_NOTIFY_UNLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_unlink)
- [var ES_EVENT_TYPE_NOTIFY_UNMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_unmount)
- [var ES_EVENT_TYPE_NOTIFY_UTIMES: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_utimes)
- [var ES_EVENT_TYPE_NOTIFY_WRITE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_write)

###### Enumeration Marker

- [var ES_EVENT_TYPE_LAST: es_event_type_t](/documentation/endpointsecurity/es_event_type_last)

###### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_event_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_event_type_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_event_type_t/rawvalue)
- [var event_count: Int](/documentation/endpointsecurity/es_muted_path_t/event_count)
- [var path: es_string_token_t](/documentation/endpointsecurity/es_muted_path_t/path)
- [es_string_token_t](/documentation/endpointsecurity/es_string_token_t)

###### Initializers

- [init()](/documentation/endpointsecurity/es_string_token_t/init())
- [init(length: Int, data: UnsafePointer<CChar>!)](/documentation/endpointsecurity/es_string_token_t/init(length:data:))

###### Inspecting the Token

- [var data: UnsafePointer<CChar>!](/documentation/endpointsecurity/es_string_token_t/data)
- [var length: Int](/documentation/endpointsecurity/es_string_token_t/length)

##### Initializers

- [init()](/documentation/endpointsecurity/es_muted_path_t/init())
- [init(type: es_mute_path_type_t, event_count: Int, events: UnsafePointer<es_event_type_t>!, path: es_string_token_t)](/documentation/endpointsecurity/es_muted_path_t/init(type:event_count:events:path:))
- [var count: Int](/documentation/endpointsecurity/es_muted_paths_t/count)

#### Initializers

- [init()](/documentation/endpointsecurity/es_muted_paths_t/init())
- [init(count: Int, paths: UnsafePointer<es_muted_path_t>!)](/documentation/endpointsecurity/es_muted_paths_t/init(count:paths:))
- [func es_release_muted_paths(UnsafeMutablePointer<es_muted_paths_t>)](/documentation/endpointsecurity/es_release_muted_paths(_:))

### Unmuting Events

- [func es_unmute_process(OpaquePointer, UnsafePointer<audit_token_t>) -> es_return_t](/documentation/endpointsecurity/es_unmute_process(_:_:))
- [func es_unmute_process_events(OpaquePointer, UnsafePointer<audit_token_t>, UnsafePointer<es_event_type_t>, Int) -> es_return_t](/documentation/endpointsecurity/es_unmute_process_events(_:_:_:_:))
- [func es_unmute_path(OpaquePointer, UnsafePointer<CChar>, es_mute_path_type_t) -> es_return_t](/documentation/endpointsecurity/es_unmute_path(_:_:_:))
- [func es_unmute_path_events(OpaquePointer, UnsafePointer<CChar>, es_mute_path_type_t, UnsafePointer<es_event_type_t>, Int) -> es_return_t](/documentation/endpointsecurity/es_unmute_path_events(_:_:_:_:_:))
- [es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_t)

#### Path Types

- [var ES_MUTE_PATH_TYPE_PREFIX: es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_prefix)
- [var ES_MUTE_PATH_TYPE_LITERAL: es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_literal)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_mute_path_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_mute_path_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_mute_path_type_t/rawvalue)
- [func es_unmute_all_paths(OpaquePointer) -> es_return_t](/documentation/endpointsecurity/es_unmute_all_paths(_:))

### Deprecated Functions

- [func es_muted_processes(OpaquePointer, UnsafeMutablePointer<Int>, UnsafeMutablePointer<UnsafeMutablePointer<audit_token_t>>?) -> es_return_t](/documentation/endpointsecurity/es_muted_processes(_:_:_:))
- [func es_mute_path_literal(OpaquePointer, UnsafePointer<CChar>) -> es_return_t](/documentation/endpointsecurity/es_mute_path_literal(_:_:))
- [func es_mute_path_prefix(OpaquePointer, UnsafePointer<CChar>) -> es_return_t](/documentation/endpointsecurity/es_mute_path_prefix(_:_:))

### Supporting Types

- [es_return_t](/documentation/endpointsecurity/es_return_t)

#### Return Values

- [var ES_RETURN_SUCCESS: es_return_t](/documentation/endpointsecurity/es_return_success)
- [var ES_RETURN_ERROR: es_return_t](/documentation/endpointsecurity/es_return_error)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_return_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_return_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_return_t/rawvalue)
- [Message](/documentation/endpointsecurity/message)

### Inspecting Messages

- [es_message_t](/documentation/endpointsecurity/es_message_t)

#### Inspecting Message Properties

- [var action: es_message_t.__Unnamed_union_action](/documentation/endpointsecurity/es_message_t/action)
- [var action_type: es_action_type_t](/documentation/endpointsecurity/es_message_t/action_type)
- [es_action_type_t](/documentation/endpointsecurity/es_action_type_t)

##### Action Types

- [var ES_ACTION_TYPE_AUTH: es_action_type_t](/documentation/endpointsecurity/es_action_type_auth)
- [var ES_ACTION_TYPE_NOTIFY: es_action_type_t](/documentation/endpointsecurity/es_action_type_notify)

##### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_action_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_action_type_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_action_type_t/rawvalue)
- [es_event_id_t](/documentation/endpointsecurity/es_event_id_t)

##### Reserved Fields

- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_id_t/reserved)

##### Initializers

- [init()](/documentation/endpointsecurity/es_event_id_t/init())
- [init(reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_id_t/init(reserved:))
- [es_result_t](/documentation/endpointsecurity/es_result_t)

##### Inspecting Result Properties

- [var result: es_result_t.__Unnamed_union_result](/documentation/endpointsecurity/es_result_t/result)
- [var result_type: es_result_type_t](/documentation/endpointsecurity/es_result_t/result_type)
- [es_result_type_t](/documentation/endpointsecurity/es_result_type_t)

###### Result Types

- [var ES_RESULT_TYPE_AUTH: es_result_type_t](/documentation/endpointsecurity/es_result_type_auth)
- [var ES_RESULT_TYPE_FLAGS: es_result_type_t](/documentation/endpointsecurity/es_result_type_flags)

###### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_result_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_result_type_t/init(rawvalue:))

###### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_result_type_t/rawvalue)

##### Initializers

- [init()](/documentation/endpointsecurity/es_result_t/init())
- [init(result_type: es_result_type_t, result: es_result_t.__Unnamed_union_result)](/documentation/endpointsecurity/es_result_t/init(result_type:result:))
- [var version: UInt32](/documentation/endpointsecurity/es_message_t/version)

#### Identifying the Matched Event

- [var event: es_events_t](/documentation/endpointsecurity/es_message_t/event)
- [es_events_t](/documentation/endpointsecurity/es_events_t)

##### File-System Events

- [var access: es_event_access_t](/documentation/endpointsecurity/es_events_t/access)
- [var clone: es_event_clone_t](/documentation/endpointsecurity/es_events_t/clone)
- [var copyfile: es_event_copyfile_t](/documentation/endpointsecurity/es_events_t/copyfile)
- [var close: es_event_close_t](/documentation/endpointsecurity/es_events_t/close)
- [var create: es_event_create_t](/documentation/endpointsecurity/es_events_t/create)
- [var dup: es_event_dup_t](/documentation/endpointsecurity/es_events_t/dup)
- [var exchangedata: es_event_exchangedata_t](/documentation/endpointsecurity/es_events_t/exchangedata)
- [var fcntl: es_event_fcntl_t](/documentation/endpointsecurity/es_events_t/fcntl)
- [var open: es_event_open_t](/documentation/endpointsecurity/es_events_t/open)
- [var rename: es_event_rename_t](/documentation/endpointsecurity/es_events_t/rename)
- [var write: es_event_write_t](/documentation/endpointsecurity/es_events_t/write)
- [var truncate: es_event_truncate_t](/documentation/endpointsecurity/es_events_t/truncate)
- [var lookup: es_event_lookup_t](/documentation/endpointsecurity/es_events_t/lookup)
- [var searchfs: es_event_searchfs_t](/documentation/endpointsecurity/es_events_t/searchfs)

##### File Metadata Events

- [var deleteextattr: es_event_deleteextattr_t](/documentation/endpointsecurity/es_events_t/deleteextattr)
- [var fsgetpath: es_event_fsgetpath_t](/documentation/endpointsecurity/es_events_t/fsgetpath)
- [var getattrlist: es_event_getattrlist_t](/documentation/endpointsecurity/es_events_t/getattrlist)
- [var getextattr: es_event_getextattr_t](/documentation/endpointsecurity/es_events_t/getextattr)
- [var listextattr: es_event_listextattr_t](/documentation/endpointsecurity/es_events_t/listextattr)
- [var readdir: es_event_readdir_t](/documentation/endpointsecurity/es_events_t/readdir)
- [var setacl: es_event_setacl_t](/documentation/endpointsecurity/es_events_t/setacl)
- [var setattrlist: es_event_setattrlist_t](/documentation/endpointsecurity/es_events_t/setattrlist)
- [var setextattr: es_event_setextattr_t](/documentation/endpointsecurity/es_events_t/setextattr)
- [var setflags: es_event_setflags_t](/documentation/endpointsecurity/es_events_t/setflags)
- [var setmode: es_event_setmode_t](/documentation/endpointsecurity/es_events_t/setmode)
- [var setowner: es_event_setowner_t](/documentation/endpointsecurity/es_events_t/setowner)
- [var stat: es_event_stat_t](/documentation/endpointsecurity/es_events_t/stat)
- [var utimes: es_event_utimes_t](/documentation/endpointsecurity/es_events_t/utimes)

##### File Provider Events

- [var file_provider_materialize: es_event_file_provider_materialize_t](/documentation/endpointsecurity/es_events_t/file_provider_materialize)
- [var file_provider_update: es_event_file_provider_update_t](/documentation/endpointsecurity/es_events_t/file_provider_update)

##### Symbolic Link Events

- [var link: es_event_link_t](/documentation/endpointsecurity/es_events_t/link)
- [var readlink: es_event_readlink_t](/documentation/endpointsecurity/es_events_t/readlink)
- [var unlink: es_event_unlink_t](/documentation/endpointsecurity/es_events_t/unlink)

##### File System Mounting Events

- [var mount: es_event_mount_t](/documentation/endpointsecurity/es_events_t/mount)
- [var unmount: es_event_unmount_t](/documentation/endpointsecurity/es_events_t/unmount)
- [var remount: es_event_remount_t](/documentation/endpointsecurity/es_events_t/remount)

##### Memory Mapping Events

- [var mmap: es_event_mmap_t](/documentation/endpointsecurity/es_events_t/mmap)
- [var mprotect: es_event_mprotect_t](/documentation/endpointsecurity/es_events_t/mprotect)

##### Process Events

- [var chdir: es_event_chdir_t](/documentation/endpointsecurity/es_events_t/chdir)
- [var chroot: es_event_chroot_t](/documentation/endpointsecurity/es_events_t/chroot)
- [var exec: es_event_exec_t](/documentation/endpointsecurity/es_events_t/exec)
- [var fork: es_event_fork_t](/documentation/endpointsecurity/es_events_t/fork)
- [var proc_check: es_event_proc_check_t](/documentation/endpointsecurity/es_events_t/proc_check)
- [var signal: es_event_signal_t](/documentation/endpointsecurity/es_events_t/signal)
- [var exit: es_event_exit_t](/documentation/endpointsecurity/es_events_t/exit)

##### Interprocess Events

- [var proc_suspend_resume: es_event_proc_suspend_resume_t](/documentation/endpointsecurity/es_events_t/proc_suspend_resume)
- [var trace: es_event_trace_t](/documentation/endpointsecurity/es_events_t/trace)
- [var remote_thread_create: es_event_remote_thread_create_t](/documentation/endpointsecurity/es_events_t/remote_thread_create)

##### Task Port Events

- [var get_task: es_event_get_task_t](/documentation/endpointsecurity/es_events_t/get_task)
- [var get_task_read: es_event_get_task_read_t](/documentation/endpointsecurity/es_events_t/get_task_read)
- [var get_task_inspect: es_event_get_task_inspect_t](/documentation/endpointsecurity/es_events_t/get_task_inspect)
- [var get_task_name: es_event_get_task_name_t](/documentation/endpointsecurity/es_events_t/get_task_name)

##### User and Group ID Events

- [var setuid: es_event_setuid_t](/documentation/endpointsecurity/es_events_t/setuid)
- [var setgid: es_event_setgid_t](/documentation/endpointsecurity/es_events_t/setgid)
- [var seteuid: es_event_seteuid_t](/documentation/endpointsecurity/es_events_t/seteuid)
- [var setegid: es_event_setegid_t](/documentation/endpointsecurity/es_events_t/setegid)
- [var setreuid: es_event_setreuid_t](/documentation/endpointsecurity/es_events_t/setreuid)
- [var setregid: es_event_setregid_t](/documentation/endpointsecurity/es_events_t/setregid)

##### Code Signing Events

- [var cs_invalidated: es_event_cs_invalidated_t](/documentation/endpointsecurity/es_events_t/cs_invalidated)

##### Socket Events

- [var uipc_bind: es_event_uipc_bind_t](/documentation/endpointsecurity/es_events_t/uipc_bind)
- [var uipc_connect: es_event_uipc_connect_t](/documentation/endpointsecurity/es_events_t/uipc_connect)

##### Clock Events

- [var settime: es_event_settime_t](/documentation/endpointsecurity/es_events_t/settime)

##### Kernel Events

- [var iokit_open: es_event_iokit_open_t](/documentation/endpointsecurity/es_events_t/iokit_open)
- [var kextload: es_event_kextload_t](/documentation/endpointsecurity/es_events_t/kextload)
- [var kextunload: es_event_kextunload_t](/documentation/endpointsecurity/es_events_t/kextunload)

##### Pseudoterminal Events

- [var pty_close: es_event_pty_close_t](/documentation/endpointsecurity/es_events_t/pty_close)
- [var pty_grant: es_event_pty_grant_t](/documentation/endpointsecurity/es_events_t/pty_grant)

##### Initializers

- [init(access: es_event_access_t)](/documentation/endpointsecurity/es_events_t/init(access:))
- [init(authentication: UnsafeMutablePointer<es_event_authentication_t>)](/documentation/endpointsecurity/es_events_t/init(authentication:))
- [init(authorization_judgement: UnsafeMutablePointer<es_event_authorization_judgement_t>)](/documentation/endpointsecurity/es_events_t/init(authorization_judgement:))
- [init(authorization_petition: UnsafeMutablePointer<es_event_authorization_petition_t>)](/documentation/endpointsecurity/es_events_t/init(authorization_petition:))
- [init(btm_launch_item_add: UnsafeMutablePointer<es_event_btm_launch_item_add_t>)](/documentation/endpointsecurity/es_events_t/init(btm_launch_item_add:))
- [init(btm_launch_item_remove: UnsafeMutablePointer<es_event_btm_launch_item_remove_t>)](/documentation/endpointsecurity/es_events_t/init(btm_launch_item_remove:))
- [init(chdir: es_event_chdir_t)](/documentation/endpointsecurity/es_events_t/init(chdir:))
- [init(chroot: es_event_chroot_t)](/documentation/endpointsecurity/es_events_t/init(chroot:))
- [init(clone: es_event_clone_t)](/documentation/endpointsecurity/es_events_t/init(clone:))
- [init(close: es_event_close_t)](/documentation/endpointsecurity/es_events_t/init(close:))
- [init(copyfile: es_event_copyfile_t)](/documentation/endpointsecurity/es_events_t/init(copyfile:))
- [init(create: es_event_create_t)](/documentation/endpointsecurity/es_events_t/init(create:))
- [init(cs_invalidated: es_event_cs_invalidated_t)](/documentation/endpointsecurity/es_events_t/init(cs_invalidated:))
- [init(deleteextattr: es_event_deleteextattr_t)](/documentation/endpointsecurity/es_events_t/init(deleteextattr:))
- [init(dup: es_event_dup_t)](/documentation/endpointsecurity/es_events_t/init(dup:))
- [init(exchangedata: es_event_exchangedata_t)](/documentation/endpointsecurity/es_events_t/init(exchangedata:))
- [init(exec: es_event_exec_t)](/documentation/endpointsecurity/es_events_t/init(exec:))
- [init(exit: es_event_exit_t)](/documentation/endpointsecurity/es_events_t/init(exit:))
- [init(fcntl: es_event_fcntl_t)](/documentation/endpointsecurity/es_events_t/init(fcntl:))
- [init(file_provider_materialize: es_event_file_provider_materialize_t)](/documentation/endpointsecurity/es_events_t/init(file_provider_materialize:))
- [init(file_provider_update: es_event_file_provider_update_t)](/documentation/endpointsecurity/es_events_t/init(file_provider_update:))
- [init(fork: es_event_fork_t)](/documentation/endpointsecurity/es_events_t/init(fork:))
- [init(fsgetpath: es_event_fsgetpath_t)](/documentation/endpointsecurity/es_events_t/init(fsgetpath:))
- [init(gatekeeper_user_override: UnsafeMutablePointer<es_event_gatekeeper_user_override_t>)](/documentation/endpointsecurity/es_events_t/init(gatekeeper_user_override:))
- [init(get_task: es_event_get_task_t)](/documentation/endpointsecurity/es_events_t/init(get_task:))
- [init(get_task_inspect: es_event_get_task_inspect_t)](/documentation/endpointsecurity/es_events_t/init(get_task_inspect:))
- [init(get_task_name: es_event_get_task_name_t)](/documentation/endpointsecurity/es_events_t/init(get_task_name:))
- [init(get_task_read: es_event_get_task_read_t)](/documentation/endpointsecurity/es_events_t/init(get_task_read:))
- [init(getattrlist: es_event_getattrlist_t)](/documentation/endpointsecurity/es_events_t/init(getattrlist:))
- [init(getextattr: es_event_getextattr_t)](/documentation/endpointsecurity/es_events_t/init(getextattr:))
- [init(iokit_open: es_event_iokit_open_t)](/documentation/endpointsecurity/es_events_t/init(iokit_open:))
- [init(kextload: es_event_kextload_t)](/documentation/endpointsecurity/es_events_t/init(kextload:))
- [init(kextunload: es_event_kextunload_t)](/documentation/endpointsecurity/es_events_t/init(kextunload:))
- [init(link: es_event_link_t)](/documentation/endpointsecurity/es_events_t/init(link:))
- [init(listextattr: es_event_listextattr_t)](/documentation/endpointsecurity/es_events_t/init(listextattr:))
- [init(login_login: UnsafeMutablePointer<es_event_login_login_t>)](/documentation/endpointsecurity/es_events_t/init(login_login:))
- [init(login_logout: UnsafeMutablePointer<es_event_login_logout_t>)](/documentation/endpointsecurity/es_events_t/init(login_logout:))
- [init(lookup: es_event_lookup_t)](/documentation/endpointsecurity/es_events_t/init(lookup:))
- [init(lw_session_lock: UnsafeMutablePointer<es_event_lw_session_lock_t>)](/documentation/endpointsecurity/es_events_t/init(lw_session_lock:))
- [init(lw_session_login: UnsafeMutablePointer<es_event_lw_session_login_t>)](/documentation/endpointsecurity/es_events_t/init(lw_session_login:))
- [init(lw_session_logout: UnsafeMutablePointer<es_event_lw_session_logout_t>)](/documentation/endpointsecurity/es_events_t/init(lw_session_logout:))
- [init(lw_session_unlock: UnsafeMutablePointer<es_event_lw_session_unlock_t>)](/documentation/endpointsecurity/es_events_t/init(lw_session_unlock:))
- [init(mmap: es_event_mmap_t)](/documentation/endpointsecurity/es_events_t/init(mmap:))
- [init(mount: es_event_mount_t)](/documentation/endpointsecurity/es_events_t/init(mount:))
- [init(mprotect: es_event_mprotect_t)](/documentation/endpointsecurity/es_events_t/init(mprotect:))
- [init(od_attribute_set: UnsafeMutablePointer<es_event_od_attribute_set_t>)](/documentation/endpointsecurity/es_events_t/init(od_attribute_set:))
- [init(od_attribute_value_add: UnsafeMutablePointer<es_event_od_attribute_value_add_t>)](/documentation/endpointsecurity/es_events_t/init(od_attribute_value_add:))
- [init(od_attribute_value_remove: UnsafeMutablePointer<es_event_od_attribute_value_remove_t>)](/documentation/endpointsecurity/es_events_t/init(od_attribute_value_remove:))
- [init(od_create_group: UnsafeMutablePointer<es_event_od_create_group_t>)](/documentation/endpointsecurity/es_events_t/init(od_create_group:))
- [init(od_create_user: UnsafeMutablePointer<es_event_od_create_user_t>)](/documentation/endpointsecurity/es_events_t/init(od_create_user:))
- [init(od_delete_group: UnsafeMutablePointer<es_event_od_delete_group_t>)](/documentation/endpointsecurity/es_events_t/init(od_delete_group:))
- [init(od_delete_user: UnsafeMutablePointer<es_event_od_delete_user_t>)](/documentation/endpointsecurity/es_events_t/init(od_delete_user:))
- [init(od_disable_user: UnsafeMutablePointer<es_event_od_disable_user_t>)](/documentation/endpointsecurity/es_events_t/init(od_disable_user:))
- [init(od_enable_user: UnsafeMutablePointer<es_event_od_enable_user_t>)](/documentation/endpointsecurity/es_events_t/init(od_enable_user:))
- [init(od_group_add: UnsafeMutablePointer<es_event_od_group_add_t>)](/documentation/endpointsecurity/es_events_t/init(od_group_add:))
- [init(od_group_remove: UnsafeMutablePointer<es_event_od_group_remove_t>)](/documentation/endpointsecurity/es_events_t/init(od_group_remove:))
- [init(od_group_set: UnsafeMutablePointer<es_event_od_group_set_t>)](/documentation/endpointsecurity/es_events_t/init(od_group_set:))
- [init(od_modify_password: UnsafeMutablePointer<es_event_od_modify_password_t>)](/documentation/endpointsecurity/es_events_t/init(od_modify_password:))
- [init(open: es_event_open_t)](/documentation/endpointsecurity/es_events_t/init(open:))
- [init(openssh_login: UnsafeMutablePointer<es_event_openssh_login_t>)](/documentation/endpointsecurity/es_events_t/init(openssh_login:))
- [init(openssh_logout: UnsafeMutablePointer<es_event_openssh_logout_t>)](/documentation/endpointsecurity/es_events_t/init(openssh_logout:))
- [init(proc_check: es_event_proc_check_t)](/documentation/endpointsecurity/es_events_t/init(proc_check:))
- [init(proc_suspend_resume: es_event_proc_suspend_resume_t)](/documentation/endpointsecurity/es_events_t/init(proc_suspend_resume:))
- [init(profile_add: UnsafeMutablePointer<es_event_profile_add_t>)](/documentation/endpointsecurity/es_events_t/init(profile_add:))
- [init(profile_remove: UnsafeMutablePointer<es_event_profile_remove_t>)](/documentation/endpointsecurity/es_events_t/init(profile_remove:))
- [init(pty_close: es_event_pty_close_t)](/documentation/endpointsecurity/es_events_t/init(pty_close:))
- [init(pty_grant: es_event_pty_grant_t)](/documentation/endpointsecurity/es_events_t/init(pty_grant:))
- [init(readdir: es_event_readdir_t)](/documentation/endpointsecurity/es_events_t/init(readdir:))
- [init(readlink: es_event_readlink_t)](/documentation/endpointsecurity/es_events_t/init(readlink:))
- [init(remote_thread_create: es_event_remote_thread_create_t)](/documentation/endpointsecurity/es_events_t/init(remote_thread_create:))
- [init(remount: es_event_remount_t)](/documentation/endpointsecurity/es_events_t/init(remount:))
- [init(rename: es_event_rename_t)](/documentation/endpointsecurity/es_events_t/init(rename:))
- [init(screensharing_attach: UnsafeMutablePointer<es_event_screensharing_attach_t>)](/documentation/endpointsecurity/es_events_t/init(screensharing_attach:))
- [init(screensharing_detach: UnsafeMutablePointer<es_event_screensharing_detach_t>)](/documentation/endpointsecurity/es_events_t/init(screensharing_detach:))
- [init(searchfs: es_event_searchfs_t)](/documentation/endpointsecurity/es_events_t/init(searchfs:))
- [init(setacl: es_event_setacl_t)](/documentation/endpointsecurity/es_events_t/init(setacl:))
- [init(setattrlist: es_event_setattrlist_t)](/documentation/endpointsecurity/es_events_t/init(setattrlist:))
- [init(setegid: es_event_setegid_t)](/documentation/endpointsecurity/es_events_t/init(setegid:))
- [init(seteuid: es_event_seteuid_t)](/documentation/endpointsecurity/es_events_t/init(seteuid:))
- [init(setextattr: es_event_setextattr_t)](/documentation/endpointsecurity/es_events_t/init(setextattr:))
- [init(setflags: es_event_setflags_t)](/documentation/endpointsecurity/es_events_t/init(setflags:))
- [init(setgid: es_event_setgid_t)](/documentation/endpointsecurity/es_events_t/init(setgid:))
- [init(setmode: es_event_setmode_t)](/documentation/endpointsecurity/es_events_t/init(setmode:))
- [init(setowner: es_event_setowner_t)](/documentation/endpointsecurity/es_events_t/init(setowner:))
- [init(setregid: es_event_setregid_t)](/documentation/endpointsecurity/es_events_t/init(setregid:))
- [init(setreuid: es_event_setreuid_t)](/documentation/endpointsecurity/es_events_t/init(setreuid:))
- [init(settime: es_event_settime_t)](/documentation/endpointsecurity/es_events_t/init(settime:))
- [init(setuid: es_event_setuid_t)](/documentation/endpointsecurity/es_events_t/init(setuid:))
- [init(signal: es_event_signal_t)](/documentation/endpointsecurity/es_events_t/init(signal:))
- [init(stat: es_event_stat_t)](/documentation/endpointsecurity/es_events_t/init(stat:))
- [init(su: UnsafeMutablePointer<es_event_su_t>)](/documentation/endpointsecurity/es_events_t/init(su:))
- [init(sudo: UnsafeMutablePointer<es_event_sudo_t>)](/documentation/endpointsecurity/es_events_t/init(sudo:))
- [init(tcc_modify: UnsafeMutablePointer<es_event_tcc_modify_t>)](/documentation/endpointsecurity/es_events_t/init(tcc_modify:))
- [init(trace: es_event_trace_t)](/documentation/endpointsecurity/es_events_t/init(trace:))
- [init(truncate: es_event_truncate_t)](/documentation/endpointsecurity/es_events_t/init(truncate:))
- [init(uipc_bind: es_event_uipc_bind_t)](/documentation/endpointsecurity/es_events_t/init(uipc_bind:))
- [init(uipc_connect: es_event_uipc_connect_t)](/documentation/endpointsecurity/es_events_t/init(uipc_connect:))
- [init(unlink: es_event_unlink_t)](/documentation/endpointsecurity/es_events_t/init(unlink:))
- [init(unmount: es_event_unmount_t)](/documentation/endpointsecurity/es_events_t/init(unmount:))
- [init(utimes: es_event_utimes_t)](/documentation/endpointsecurity/es_events_t/init(utimes:))
- [init(write: es_event_write_t)](/documentation/endpointsecurity/es_events_t/init(write:))
- [init(xp_malware_detected: UnsafeMutablePointer<es_event_xp_malware_detected_t>)](/documentation/endpointsecurity/es_events_t/init(xp_malware_detected:))
- [init(xp_malware_remediated: UnsafeMutablePointer<es_event_xp_malware_remediated_t>)](/documentation/endpointsecurity/es_events_t/init(xp_malware_remediated:))
- [init(xpc_connect: UnsafeMutablePointer<es_event_xpc_connect_t>)](/documentation/endpointsecurity/es_events_t/init(xpc_connect:))

##### Instance Properties

- [var authentication: UnsafeMutablePointer<es_event_authentication_t>](/documentation/endpointsecurity/es_events_t/authentication)
- [var authorization_judgement: UnsafeMutablePointer<es_event_authorization_judgement_t>](/documentation/endpointsecurity/es_events_t/authorization_judgement)
- [var authorization_petition: UnsafeMutablePointer<es_event_authorization_petition_t>](/documentation/endpointsecurity/es_events_t/authorization_petition)
- [var btm_launch_item_add: UnsafeMutablePointer<es_event_btm_launch_item_add_t>](/documentation/endpointsecurity/es_events_t/btm_launch_item_add)
- [var btm_launch_item_remove: UnsafeMutablePointer<es_event_btm_launch_item_remove_t>](/documentation/endpointsecurity/es_events_t/btm_launch_item_remove)
- [var gatekeeper_user_override: UnsafeMutablePointer<es_event_gatekeeper_user_override_t>](/documentation/endpointsecurity/es_events_t/gatekeeper_user_override)
- [var login_login: UnsafeMutablePointer<es_event_login_login_t>](/documentation/endpointsecurity/es_events_t/login_login)
- [var login_logout: UnsafeMutablePointer<es_event_login_logout_t>](/documentation/endpointsecurity/es_events_t/login_logout)
- [var lw_session_lock: UnsafeMutablePointer<es_event_lw_session_lock_t>](/documentation/endpointsecurity/es_events_t/lw_session_lock)
- [var lw_session_login: UnsafeMutablePointer<es_event_lw_session_login_t>](/documentation/endpointsecurity/es_events_t/lw_session_login)
- [var lw_session_logout: UnsafeMutablePointer<es_event_lw_session_logout_t>](/documentation/endpointsecurity/es_events_t/lw_session_logout)
- [var lw_session_unlock: UnsafeMutablePointer<es_event_lw_session_unlock_t>](/documentation/endpointsecurity/es_events_t/lw_session_unlock)
- [var od_attribute_set: UnsafeMutablePointer<es_event_od_attribute_set_t>](/documentation/endpointsecurity/es_events_t/od_attribute_set)
- [var od_attribute_value_add: UnsafeMutablePointer<es_event_od_attribute_value_add_t>](/documentation/endpointsecurity/es_events_t/od_attribute_value_add)
- [var od_attribute_value_remove: UnsafeMutablePointer<es_event_od_attribute_value_remove_t>](/documentation/endpointsecurity/es_events_t/od_attribute_value_remove)
- [var od_create_group: UnsafeMutablePointer<es_event_od_create_group_t>](/documentation/endpointsecurity/es_events_t/od_create_group)
- [var od_create_user: UnsafeMutablePointer<es_event_od_create_user_t>](/documentation/endpointsecurity/es_events_t/od_create_user)
- [var od_delete_group: UnsafeMutablePointer<es_event_od_delete_group_t>](/documentation/endpointsecurity/es_events_t/od_delete_group)
- [var od_delete_user: UnsafeMutablePointer<es_event_od_delete_user_t>](/documentation/endpointsecurity/es_events_t/od_delete_user)
- [var od_disable_user: UnsafeMutablePointer<es_event_od_disable_user_t>](/documentation/endpointsecurity/es_events_t/od_disable_user)
- [var od_enable_user: UnsafeMutablePointer<es_event_od_enable_user_t>](/documentation/endpointsecurity/es_events_t/od_enable_user)
- [var od_group_add: UnsafeMutablePointer<es_event_od_group_add_t>](/documentation/endpointsecurity/es_events_t/od_group_add)
- [var od_group_remove: UnsafeMutablePointer<es_event_od_group_remove_t>](/documentation/endpointsecurity/es_events_t/od_group_remove)
- [var od_group_set: UnsafeMutablePointer<es_event_od_group_set_t>](/documentation/endpointsecurity/es_events_t/od_group_set)
- [var od_modify_password: UnsafeMutablePointer<es_event_od_modify_password_t>](/documentation/endpointsecurity/es_events_t/od_modify_password)
- [var openssh_login: UnsafeMutablePointer<es_event_openssh_login_t>](/documentation/endpointsecurity/es_events_t/openssh_login)
- [var openssh_logout: UnsafeMutablePointer<es_event_openssh_logout_t>](/documentation/endpointsecurity/es_events_t/openssh_logout)
- [var profile_add: UnsafeMutablePointer<es_event_profile_add_t>](/documentation/endpointsecurity/es_events_t/profile_add)
- [var profile_remove: UnsafeMutablePointer<es_event_profile_remove_t>](/documentation/endpointsecurity/es_events_t/profile_remove)
- [var screensharing_attach: UnsafeMutablePointer<es_event_screensharing_attach_t>](/documentation/endpointsecurity/es_events_t/screensharing_attach)
- [var screensharing_detach: UnsafeMutablePointer<es_event_screensharing_detach_t>](/documentation/endpointsecurity/es_events_t/screensharing_detach)
- [var su: UnsafeMutablePointer<es_event_su_t>](/documentation/endpointsecurity/es_events_t/su)
- [var sudo: UnsafeMutablePointer<es_event_sudo_t>](/documentation/endpointsecurity/es_events_t/sudo)
- [var tcc_modify: UnsafeMutablePointer<es_event_tcc_modify_t>](/documentation/endpointsecurity/es_events_t/tcc_modify)
- [var xp_malware_detected: UnsafeMutablePointer<es_event_xp_malware_detected_t>](/documentation/endpointsecurity/es_events_t/xp_malware_detected)
- [var xp_malware_remediated: UnsafeMutablePointer<es_event_xp_malware_remediated_t>](/documentation/endpointsecurity/es_events_t/xp_malware_remediated)
- [var xpc_connect: UnsafeMutablePointer<es_event_xpc_connect_t>](/documentation/endpointsecurity/es_events_t/xpc_connect)
- [var event_type: es_event_type_t](/documentation/endpointsecurity/es_message_t/event_type)
- [es_event_type_t](/documentation/endpointsecurity/es_event_type_t)

##### Authorization Event Types

- [var ES_EVENT_TYPE_AUTH_CHDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_chdir)
- [var ES_EVENT_TYPE_AUTH_CHROOT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_chroot)
- [var ES_EVENT_TYPE_AUTH_CLONE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_clone)
- [var ES_EVENT_TYPE_AUTH_COPYFILE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_copyfile)
- [var ES_EVENT_TYPE_AUTH_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_create)
- [var ES_EVENT_TYPE_AUTH_DELETEEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_deleteextattr)
- [var ES_EVENT_TYPE_AUTH_EXCHANGEDATA: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_exchangedata)
- [var ES_EVENT_TYPE_AUTH_EXEC: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_exec)
- [var ES_EVENT_TYPE_AUTH_FCNTL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_fcntl)
- [var ES_EVENT_TYPE_AUTH_FILE_PROVIDER_MATERIALIZE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_file_provider_materialize)
- [var ES_EVENT_TYPE_AUTH_FILE_PROVIDER_UPDATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_file_provider_update)
- [var ES_EVENT_TYPE_AUTH_FSGETPATH: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_fsgetpath)
- [var ES_EVENT_TYPE_AUTH_GET_TASK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_get_task)
- [var ES_EVENT_TYPE_AUTH_GET_TASK_READ: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_get_task_read)
- [var ES_EVENT_TYPE_AUTH_GETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_getattrlist)
- [var ES_EVENT_TYPE_AUTH_GETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_getextattr)
- [var ES_EVENT_TYPE_AUTH_IOKIT_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_iokit_open)
- [var ES_EVENT_TYPE_AUTH_KEXTLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_kextload)
- [var ES_EVENT_TYPE_AUTH_LINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_link)
- [var ES_EVENT_TYPE_AUTH_LISTEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_listextattr)
- [var ES_EVENT_TYPE_AUTH_MMAP: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mmap)
- [var ES_EVENT_TYPE_AUTH_MOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mount)
- [var ES_EVENT_TYPE_AUTH_MPROTECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_mprotect)
- [var ES_EVENT_TYPE_AUTH_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_open)
- [var ES_EVENT_TYPE_AUTH_PROC_CHECK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_proc_check)
- [var ES_EVENT_TYPE_AUTH_PROC_SUSPEND_RESUME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_proc_suspend_resume)
- [var ES_EVENT_TYPE_AUTH_READDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_readdir)
- [var ES_EVENT_TYPE_AUTH_READLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_readlink)
- [var ES_EVENT_TYPE_AUTH_REMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_remount)
- [var ES_EVENT_TYPE_AUTH_RENAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_rename)
- [var ES_EVENT_TYPE_AUTH_SEARCHFS: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_searchfs)
- [var ES_EVENT_TYPE_AUTH_SETACL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setacl)
- [var ES_EVENT_TYPE_AUTH_SETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setattrlist)
- [var ES_EVENT_TYPE_AUTH_SETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setextattr)
- [var ES_EVENT_TYPE_AUTH_SETFLAGS: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setflags)
- [var ES_EVENT_TYPE_AUTH_SETMODE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setmode)
- [var ES_EVENT_TYPE_AUTH_SETOWNER: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_setowner)
- [var ES_EVENT_TYPE_AUTH_SETTIME: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_settime)
- [var ES_EVENT_TYPE_AUTH_SIGNAL: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_signal)
- [var ES_EVENT_TYPE_AUTH_TRUNCATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_truncate)
- [var ES_EVENT_TYPE_AUTH_UIPC_BIND: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_uipc_bind)
- [var ES_EVENT_TYPE_AUTH_UIPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_uipc_connect)
- [var ES_EVENT_TYPE_AUTH_UNLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_unlink)
- [var ES_EVENT_TYPE_AUTH_UTIMES: es_event_type_t](/documentation/endpointsecurity/es_event_type_auth_utimes)

##### Notification Event Types

- [var ES_EVENT_TYPE_NOTIFY_ACCESS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_access)
- [var ES_EVENT_TYPE_NOTIFY_CHDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_chdir)
- [var ES_EVENT_TYPE_NOTIFY_CHROOT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_chroot)
- [var ES_EVENT_TYPE_NOTIFY_CLONE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_clone)
- [var ES_EVENT_TYPE_NOTIFY_CLOSE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_close)
- [var ES_EVENT_TYPE_NOTIFY_COPYFILE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_copyfile)
- [var ES_EVENT_TYPE_NOTIFY_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_create)
- [var ES_EVENT_TYPE_NOTIFY_CS_INVALIDATED: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_cs_invalidated)
- [var ES_EVENT_TYPE_NOTIFY_DELETEEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_deleteextattr)
- [var ES_EVENT_TYPE_NOTIFY_DUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_dup)
- [var ES_EVENT_TYPE_NOTIFY_EXCHANGEDATA: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exchangedata)
- [var ES_EVENT_TYPE_NOTIFY_EXEC: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exec)
- [var ES_EVENT_TYPE_NOTIFY_EXIT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_exit)
- [var ES_EVENT_TYPE_NOTIFY_FCNTL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fcntl)
- [var ES_EVENT_TYPE_NOTIFY_FILE_PROVIDER_MATERIALIZE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_file_provider_materialize)
- [var ES_EVENT_TYPE_NOTIFY_FILE_PROVIDER_UPDATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_file_provider_update)
- [var ES_EVENT_TYPE_NOTIFY_FORK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fork)
- [var ES_EVENT_TYPE_NOTIFY_FSGETPATH: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_fsgetpath)
- [var ES_EVENT_TYPE_NOTIFY_GETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_getattrlist)
- [var ES_EVENT_TYPE_NOTIFY_GETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_getextattr)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_READ: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_read)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_INSPECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_inspect)
- [var ES_EVENT_TYPE_NOTIFY_GET_TASK_NAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_get_task_name)
- [var ES_EVENT_TYPE_NOTIFY_IOKIT_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_iokit_open)
- [var ES_EVENT_TYPE_NOTIFY_KEXTLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_kextload)
- [var ES_EVENT_TYPE_NOTIFY_KEXTUNLOAD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_kextunload)
- [var ES_EVENT_TYPE_NOTIFY_LINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_link)
- [var ES_EVENT_TYPE_NOTIFY_LISTEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_listextattr)
- [var ES_EVENT_TYPE_NOTIFY_LOOKUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_lookup)
- [var ES_EVENT_TYPE_NOTIFY_MMAP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mmap)
- [var ES_EVENT_TYPE_NOTIFY_MOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mount)
- [var ES_EVENT_TYPE_NOTIFY_MPROTECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_mprotect)
- [var ES_EVENT_TYPE_NOTIFY_OPEN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_open)
- [var ES_EVENT_TYPE_NOTIFY_PROC_CHECK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_proc_check)
- [var ES_EVENT_TYPE_NOTIFY_PROC_SUSPEND_RESUME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_proc_suspend_resume)
- [var ES_EVENT_TYPE_NOTIFY_PTY_CLOSE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_pty_close)
- [var ES_EVENT_TYPE_NOTIFY_PTY_GRANT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_pty_grant)
- [var ES_EVENT_TYPE_NOTIFY_READDIR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_readdir)
- [var ES_EVENT_TYPE_NOTIFY_READLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_readlink)
- [var ES_EVENT_TYPE_NOTIFY_REMOTE_THREAD_CREATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_remote_thread_create)
- [var ES_EVENT_TYPE_NOTIFY_REMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_remount)
- [var ES_EVENT_TYPE_NOTIFY_RENAME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_rename)
- [var ES_EVENT_TYPE_NOTIFY_SEARCHFS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_searchfs)
- [var ES_EVENT_TYPE_NOTIFY_SETACL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setacl)
- [var ES_EVENT_TYPE_NOTIFY_SETATTRLIST: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setattrlist)
- [var ES_EVENT_TYPE_NOTIFY_SETEGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setegid)
- [var ES_EVENT_TYPE_NOTIFY_SETEUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_seteuid)
- [var ES_EVENT_TYPE_NOTIFY_SETEXTATTR: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setextattr)
- [var ES_EVENT_TYPE_NOTIFY_SETGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setgid)
- [var ES_EVENT_TYPE_NOTIFY_SETFLAGS: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setflags)
- [var ES_EVENT_TYPE_NOTIFY_SETMODE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setmode)
- [var ES_EVENT_TYPE_NOTIFY_SETOWNER: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setowner)
- [var ES_EVENT_TYPE_NOTIFY_SETREGID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setregid)
- [var ES_EVENT_TYPE_NOTIFY_SETREUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setreuid)
- [var ES_EVENT_TYPE_NOTIFY_SETTIME: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_settime)
- [var ES_EVENT_TYPE_NOTIFY_SETUID: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_setuid)
- [var ES_EVENT_TYPE_NOTIFY_SIGNAL: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_signal)
- [var ES_EVENT_TYPE_NOTIFY_STAT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_stat)
- [var ES_EVENT_TYPE_NOTIFY_TRACE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_trace)
- [var ES_EVENT_TYPE_NOTIFY_TRUNCATE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_truncate)
- [var ES_EVENT_TYPE_NOTIFY_UIPC_BIND: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_uipc_bind)
- [var ES_EVENT_TYPE_NOTIFY_UIPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_uipc_connect)
- [var ES_EVENT_TYPE_NOTIFY_UNLINK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_unlink)
- [var ES_EVENT_TYPE_NOTIFY_UNMOUNT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_unmount)
- [var ES_EVENT_TYPE_NOTIFY_UTIMES: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_utimes)
- [var ES_EVENT_TYPE_NOTIFY_WRITE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_write)

##### Enumeration Marker

- [var ES_EVENT_TYPE_LAST: es_event_type_t](/documentation/endpointsecurity/es_event_type_last)

##### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_event_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_event_type_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_event_type_t/rawvalue)

#### Inspecting Timing Properties

- [var time: timespec](/documentation/endpointsecurity/es_message_t/time)
- [var mach_time: UInt64](/documentation/endpointsecurity/es_message_t/mach_time)
- [var deadline: UInt64](/documentation/endpointsecurity/es_message_t/deadline)
- [var seq_num: UInt64](/documentation/endpointsecurity/es_message_t/seq_num)
- [var global_seq_num: UInt64](/documentation/endpointsecurity/es_message_t/global_seq_num)

#### Identifying the Source Process

- [var process: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_message_t/process)
- [es_process_t](/documentation/endpointsecurity/es_process_t)

##### Inspecting the Source Process

- [var audit_token: audit_token_t](/documentation/endpointsecurity/es_process_t/audit_token)
- [var executable: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_process_t/executable)
- [var is_es_client: Bool](/documentation/endpointsecurity/es_process_t/is_es_client)
- [var is_platform_binary: Bool](/documentation/endpointsecurity/es_process_t/is_platform_binary)
- [var start_time: timeval](/documentation/endpointsecurity/es_process_t/start_time)

##### Inspecting Process IDs

- [var ppid: pid_t](/documentation/endpointsecurity/es_process_t/ppid)
- [var original_ppid: pid_t](/documentation/endpointsecurity/es_process_t/original_ppid)
- [var group_id: pid_t](/documentation/endpointsecurity/es_process_t/group_id)
- [var session_id: pid_t](/documentation/endpointsecurity/es_process_t/session_id)
- [var tty: UnsafeMutablePointer<es_file_t>?](/documentation/endpointsecurity/es_process_t/tty)

##### Inspecting Code Signing Properties

- [var codesigning_flags: UInt32](/documentation/endpointsecurity/es_process_t/codesigning_flags)
- [var cdhash: es_cdhash_t](/documentation/endpointsecurity/es_process_t/cdhash)
- [var signing_id: es_string_token_t](/documentation/endpointsecurity/es_process_t/signing_id)
- [var team_id: es_string_token_t](/documentation/endpointsecurity/es_process_t/team_id)

##### Inspecting Audit Tokens

- [var responsible_audit_token: audit_token_t](/documentation/endpointsecurity/es_process_t/responsible_audit_token)
- [var parent_audit_token: audit_token_t](/documentation/endpointsecurity/es_process_t/parent_audit_token)

##### Initializers

- [init(audit_token: audit_token_t, ppid: pid_t, original_ppid: pid_t, group_id: pid_t, session_id: pid_t, codesigning_flags: UInt32, is_platform_binary: Bool, is_es_client: Bool, cdhash: es_cdhash_t, signing_id: es_string_token_t, team_id: es_string_token_t, executable: UnsafeMutablePointer<es_file_t>, tty: UnsafeMutablePointer<es_file_t>?, start_time: timeval, responsible_audit_token: audit_token_t, parent_audit_token: audit_token_t, cs_validation_category: es_cs_validation_category_t)](/documentation/endpointsecurity/es_process_t/init(audit_token:ppid:original_ppid:group_id:session_id:codesigning_flags:is_platform_binary:is_es_client:cdhash:signing_id:team_id:executable:tty:start_time:responsible_audit_token:parent_audit_token:cs_validation_category:))

##### Instance Properties

- [var cs_validation_category: es_cs_validation_category_t](/documentation/endpointsecurity/es_process_t/cs_validation_category)

#### Inspecting Thread Properties

- [var thread: UnsafeMutablePointer<es_thread_t>?](/documentation/endpointsecurity/es_message_t/thread)
- [es_thread_t](/documentation/endpointsecurity/es_thread_t)

##### Identifying the Thread

- [var thread_id: UInt64](/documentation/endpointsecurity/es_thread_t/thread_id)

##### Initializers

- [init()](/documentation/endpointsecurity/es_thread_t/init())
- [init(thread_id: UInt64)](/documentation/endpointsecurity/es_thread_t/init(thread_id:))

### Retaining and Releasing Messages

- [func es_retain_message(UnsafePointer<es_message_t>)](/documentation/endpointsecurity/es_retain_message(_:))
- [func es_release_message(UnsafePointer<es_message_t>)](/documentation/endpointsecurity/es_release_message(_:))

### Deprecated Functions

- [func es_copy_message(UnsafePointer<es_message_t>) -> UnsafeMutablePointer<es_message_t>?](/documentation/endpointsecurity/es_copy_message(_:))
- [func es_message_size(UnsafePointer<es_message_t>) -> Int](/documentation/endpointsecurity/es_message_size(_:))
- [func es_free_message(UnsafeMutablePointer<es_message_t>)](/documentation/endpointsecurity/es_free_message(_:))

### Supporting Types

- [es_result_t](/documentation/endpointsecurity/es_result_t)

#### Inspecting Result Properties

- [var result: es_result_t.__Unnamed_union_result](/documentation/endpointsecurity/es_result_t/result)
- [var result_type: es_result_type_t](/documentation/endpointsecurity/es_result_t/result_type)
- [es_result_type_t](/documentation/endpointsecurity/es_result_type_t)

##### Result Types

- [var ES_RESULT_TYPE_AUTH: es_result_type_t](/documentation/endpointsecurity/es_result_type_auth)
- [var ES_RESULT_TYPE_FLAGS: es_result_type_t](/documentation/endpointsecurity/es_result_type_flags)

##### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_result_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_result_type_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_result_type_t/rawvalue)

#### Initializers

- [init()](/documentation/endpointsecurity/es_result_t/init())
- [init(result_type: es_result_type_t, result: es_result_t.__Unnamed_union_result)](/documentation/endpointsecurity/es_result_t/init(result_type:result:))
- [es_string_token_t](/documentation/endpointsecurity/es_string_token_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_string_token_t/init())
- [init(length: Int, data: UnsafePointer<CChar>!)](/documentation/endpointsecurity/es_string_token_t/init(length:data:))

#### Inspecting the Token

- [var data: UnsafePointer<CChar>!](/documentation/endpointsecurity/es_string_token_t/data)
- [var length: Int](/documentation/endpointsecurity/es_string_token_t/length)
- [es_token_t](/documentation/endpointsecurity/es_token_t)

#### Inspecting the Token

- [var data: UnsafePointer<UInt8>!](/documentation/endpointsecurity/es_token_t/data)
- [var size: Int](/documentation/endpointsecurity/es_token_t/size)

#### Initializers

- [init()](/documentation/endpointsecurity/es_token_t/init())
- [init(size: Int, data: UnsafePointer<UInt8>!)](/documentation/endpointsecurity/es_token_t/init(size:data:))
- [Event Types](/documentation/endpointsecurity/event-types)

### File-System Event Types

- [es_file_t](/documentation/endpointsecurity/es_file_t)

#### Inspecting File Properties

- [var path: es_string_token_t](/documentation/endpointsecurity/es_file_t/path)
- [var path_truncated: Bool](/documentation/endpointsecurity/es_file_t/path_truncated)
- [var stat: stat](/documentation/endpointsecurity/es_file_t/stat)

#### Initializers

- [init()](/documentation/endpointsecurity/es_file_t/init())
- [init(path: es_string_token_t, path_truncated: Bool, stat: stat)](/documentation/endpointsecurity/es_file_t/init(path:path_truncated:stat:))
- [es_event_access_t](/documentation/endpointsecurity/es_event_access_t)

#### Inspecting Event Properties

- [var mode: Int32](/documentation/endpointsecurity/es_event_access_t/mode)
- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_access_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_access_t/reserved)

#### Initializers

- [init(mode: Int32, target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_access_t/init(mode:target:reserved:))
- [es_event_clone_t](/documentation/endpointsecurity/es_event_clone_t)

#### Inspecting Event Properties

- [var source: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_clone_t/source)
- [var target_dir: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_clone_t/target_dir)
- [var target_name: es_string_token_t](/documentation/endpointsecurity/es_event_clone_t/target_name)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_clone_t/reserved)

#### Initializers

- [init(source: UnsafeMutablePointer<es_file_t>, target_dir: UnsafeMutablePointer<es_file_t>, target_name: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_clone_t/init(source:target_dir:target_name:reserved:))
- [es_event_copyfile_t](/documentation/endpointsecurity/es_event_copyfile_t)

#### Inspecting Event Properties

- [var source: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_copyfile_t/source)
- [var target_file: UnsafeMutablePointer<es_file_t>?](/documentation/endpointsecurity/es_event_copyfile_t/target_file)
- [var target_dir: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_copyfile_t/target_dir)
- [var target_name: es_string_token_t](/documentation/endpointsecurity/es_event_copyfile_t/target_name)
- [var mode: mode_t](/documentation/endpointsecurity/es_event_copyfile_t/mode)
- [var flags: Int32](/documentation/endpointsecurity/es_event_copyfile_t/flags)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_copyfile_t/reserved)

#### Initializers

- [init(source: UnsafeMutablePointer<es_file_t>, target_file: UnsafeMutablePointer<es_file_t>?, target_dir: UnsafeMutablePointer<es_file_t>, target_name: es_string_token_t, mode: mode_t, flags: Int32, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_copyfile_t/init(source:target_file:target_dir:target_name:mode:flags:reserved:))
- [es_event_create_t](/documentation/endpointsecurity/es_event_create_t)

#### Inspecting Event Properties

- [var destination: es_event_create_t.__Unnamed_union_destination](/documentation/endpointsecurity/es_event_create_t/destination)
- [var destination_type: es_destination_type_t](/documentation/endpointsecurity/es_event_create_t/destination_type)
- [es_destination_type_t](/documentation/endpointsecurity/es_destination_type_t)

##### Destination Types

- [var ES_DESTINATION_TYPE_EXISTING_FILE: es_destination_type_t](/documentation/endpointsecurity/es_destination_type_existing_file)
- [var ES_DESTINATION_TYPE_NEW_PATH: es_destination_type_t](/documentation/endpointsecurity/es_destination_type_new_path)

##### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_destination_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_destination_type_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_destination_type_t/rawvalue)
- [var reserved2: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_create_t/reserved2)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_create_t/init())

#### Instance Properties

- [var acl: acl_t?](/documentation/endpointsecurity/es_event_create_t/acl-6m1ze)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_create_t/reserved-fmi7)
- [es_event_dup_t](/documentation/endpointsecurity/es_event_dup_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_dup_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_dup_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_dup_t/init(target:reserved:))
- [es_event_fcntl_t](/documentation/endpointsecurity/es_event_fcntl_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_fcntl_t/target)
- [var cmd: Int32](/documentation/endpointsecurity/es_event_fcntl_t/cmd)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_fcntl_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, cmd: Int32, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_fcntl_t/init(target:cmd:reserved:))
- [es_event_open_t](/documentation/endpointsecurity/es_event_open_t)

#### Inspecting Event Properties

- [var file: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_open_t/file)
- [var fflag: Int32](/documentation/endpointsecurity/es_event_open_t/fflag)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_open_t/reserved)

#### Initializers

- [init(fflag: Int32, file: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_open_t/init(fflag:file:reserved:))
- [es_event_close_t](/documentation/endpointsecurity/es_event_close_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_close_t/target)
- [var modified: Bool](/documentation/endpointsecurity/es_event_close_t/modified)

#### Instance Properties

- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_close_t/reserved-1vkig)
- [var was_mapped_writable: Bool](/documentation/endpointsecurity/es_event_close_t/was_mapped_writable-5iaxq)
- [es_event_rename_t](/documentation/endpointsecurity/es_event_rename_t)

#### Inspecting Event Properties

- [var source: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_rename_t/source)
- [var destination: es_event_rename_t.__Unnamed_union_destination](/documentation/endpointsecurity/es_event_rename_t/destination)
- [var destination_type: es_destination_type_t](/documentation/endpointsecurity/es_event_rename_t/destination_type)
- [es_destination_type_t](/documentation/endpointsecurity/es_destination_type_t)

##### Destination Types

- [var ES_DESTINATION_TYPE_EXISTING_FILE: es_destination_type_t](/documentation/endpointsecurity/es_destination_type_existing_file)
- [var ES_DESTINATION_TYPE_NEW_PATH: es_destination_type_t](/documentation/endpointsecurity/es_destination_type_new_path)

##### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_destination_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_destination_type_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_destination_type_t/rawvalue)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_rename_t/reserved)

#### Initializers

- [init(source: UnsafeMutablePointer<es_file_t>, destination_type: es_destination_type_t, destination: es_event_rename_t.__Unnamed_union_destination, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_rename_t/init(source:destination_type:destination:reserved:))
- [es_event_truncate_t](/documentation/endpointsecurity/es_event_truncate_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_truncate_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_truncate_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_truncate_t/init(target:reserved:))
- [es_event_exchangedata_t](/documentation/endpointsecurity/es_event_exchangedata_t)

#### Inspecting Event Properties

- [var file1: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_exchangedata_t/file1)
- [var file2: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_exchangedata_t/file2)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_exchangedata_t/reserved)

#### Initializers

- [init(file1: UnsafeMutablePointer<es_file_t>, file2: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_exchangedata_t/init(file1:file2:reserved:))
- [es_event_write_t](/documentation/endpointsecurity/es_event_write_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_write_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_write_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_write_t/init(target:reserved:))
- [es_event_lookup_t](/documentation/endpointsecurity/es_event_lookup_t)

#### Inspecting Event Properties

- [var source_dir: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_lookup_t/source_dir)
- [var relative_target: es_string_token_t](/documentation/endpointsecurity/es_event_lookup_t/relative_target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_lookup_t/reserved)

#### Initializers

- [init(source_dir: UnsafeMutablePointer<es_file_t>, relative_target: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_lookup_t/init(source_dir:relative_target:reserved:))
- [es_event_searchfs_t](/documentation/endpointsecurity/es_event_searchfs_t)

#### Inspecting Child Properties

- [var attrlist: attrlist](/documentation/endpointsecurity/es_event_searchfs_t/attrlist)
- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_searchfs_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_searchfs_t/reserved)

#### Initializers

- [init(attrlist: attrlist, target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_searchfs_t/init(attrlist:target:reserved:))

### File Metadata Event Types

- [es_event_deleteextattr_t](/documentation/endpointsecurity/es_event_deleteextattr_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_deleteextattr_t/target)
- [var extattr: es_string_token_t](/documentation/endpointsecurity/es_event_deleteextattr_t/extattr)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_deleteextattr_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, extattr: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_deleteextattr_t/init(target:extattr:reserved:))
- [es_event_fsgetpath_t](/documentation/endpointsecurity/es_event_fsgetpath_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_fsgetpath_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_fsgetpath_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_fsgetpath_t/init(target:reserved:))
- [es_event_getattrlist_t](/documentation/endpointsecurity/es_event_getattrlist_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_getattrlist_t/target)
- [var attrlist: attrlist](/documentation/endpointsecurity/es_event_getattrlist_t/attrlist)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_getattrlist_t/reserved)

#### Initializers

- [init(attrlist: attrlist, target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_getattrlist_t/init(attrlist:target:reserved:))
- [es_event_getextattr_t](/documentation/endpointsecurity/es_event_getextattr_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_getextattr_t/target)
- [var extattr: es_string_token_t](/documentation/endpointsecurity/es_event_getextattr_t/extattr)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_getextattr_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, extattr: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_getextattr_t/init(target:extattr:reserved:))
- [es_event_listextattr_t](/documentation/endpointsecurity/es_event_listextattr_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_listextattr_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_listextattr_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_listextattr_t/init(target:reserved:))
- [es_event_readdir_t](/documentation/endpointsecurity/es_event_readdir_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_readdir_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_readdir_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_readdir_t/init(target:reserved:))
- [es_event_setacl_t](/documentation/endpointsecurity/es_event_setacl_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_setacl_t/target)
- [var acl: es_event_setacl_t.__Unnamed_union_acl](/documentation/endpointsecurity/es_event_setacl_t/acl)
- [var set_or_clear: es_set_or_clear_t](/documentation/endpointsecurity/es_event_setacl_t/set_or_clear)
- [es_set_or_clear_t](/documentation/endpointsecurity/es_set_or_clear_t)

##### Event Types

- [var ES_CLEAR: es_set_or_clear_t](/documentation/endpointsecurity/es_clear)
- [var ES_SET: es_set_or_clear_t](/documentation/endpointsecurity/es_set)

##### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_set_or_clear_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_set_or_clear_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_set_or_clear_t/rawvalue)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setacl_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, set_or_clear: es_set_or_clear_t, acl: es_event_setacl_t.__Unnamed_union_acl, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setacl_t/init(target:set_or_clear:acl:reserved:))
- [es_event_setattrlist_t](/documentation/endpointsecurity/es_event_setattrlist_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_setattrlist_t/target)
- [var attrlist: attrlist](/documentation/endpointsecurity/es_event_setattrlist_t/attrlist)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setattrlist_t/reserved)

#### Initializers

- [init(attrlist: attrlist, target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setattrlist_t/init(attrlist:target:reserved:))
- [es_event_setextattr_t](/documentation/endpointsecurity/es_event_setextattr_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_setextattr_t/target)
- [var extattr: es_string_token_t](/documentation/endpointsecurity/es_event_setextattr_t/extattr)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setextattr_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, extattr: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setextattr_t/init(target:extattr:reserved:))
- [es_event_setflags_t](/documentation/endpointsecurity/es_event_setflags_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_setflags_t/target)
- [var flags: UInt32](/documentation/endpointsecurity/es_event_setflags_t/flags)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setflags_t/reserved)

#### Initializers

- [init(flags: UInt32, target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setflags_t/init(flags:target:reserved:))
- [es_event_setmode_t](/documentation/endpointsecurity/es_event_setmode_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_setmode_t/target)
- [var mode: mode_t](/documentation/endpointsecurity/es_event_setmode_t/mode)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setmode_t/reserved)

#### Initializers

- [init(mode: mode_t, target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setmode_t/init(mode:target:reserved:))
- [es_event_setowner_t](/documentation/endpointsecurity/es_event_setowner_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_setowner_t/target)
- [var uid: uid_t](/documentation/endpointsecurity/es_event_setowner_t/uid)
- [var gid: gid_t](/documentation/endpointsecurity/es_event_setowner_t/gid)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setowner_t/reserved)

#### Initializers

- [init(uid: uid_t, gid: gid_t, target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setowner_t/init(uid:gid:target:reserved:))
- [es_event_stat_t](/documentation/endpointsecurity/es_event_stat_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_stat_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_stat_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_stat_t/init(target:reserved:))
- [es_event_utimes_t](/documentation/endpointsecurity/es_event_utimes_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_utimes_t/target)
- [var atime: timespec](/documentation/endpointsecurity/es_event_utimes_t/atime)
- [var mtime: timespec](/documentation/endpointsecurity/es_event_utimes_t/mtime)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_utimes_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, atime: timespec, mtime: timespec, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_utimes_t/init(target:atime:mtime:reserved:))

### File Provider Event Types

- [es_event_file_provider_materialize_t](/documentation/endpointsecurity/es_event_file_provider_materialize_t)

#### Inspecting Event Properties

- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_file_provider_materialize_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_file_provider_materialize_t/instigator_token)
- [var source: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_file_provider_materialize_t/source)
- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_file_provider_materialize_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_file_provider_materialize_t/reserved)

#### Initializers

- [init(instigator: UnsafeMutablePointer<es_process_t>?, source: UnsafeMutablePointer<es_file_t>, target: UnsafeMutablePointer<es_file_t>, instigator_token: audit_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_file_provider_materialize_t/init(instigator:source:target:instigator_token:reserved:))
- [es_event_file_provider_update_t](/documentation/endpointsecurity/es_event_file_provider_update_t)

#### Inspecting Event Properties

- [var source: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_file_provider_update_t/source)
- [var target_path: es_string_token_t](/documentation/endpointsecurity/es_event_file_provider_update_t/target_path)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_file_provider_update_t/reserved)

#### Initializers

- [init(source: UnsafeMutablePointer<es_file_t>, target_path: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_file_provider_update_t/init(source:target_path:reserved:))

### Link Event Types

- [es_event_link_t](/documentation/endpointsecurity/es_event_link_t)

#### Inspecting Event Properties

- [var source: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_link_t/source)
- [var target_dir: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_link_t/target_dir)
- [var target_filename: es_string_token_t](/documentation/endpointsecurity/es_event_link_t/target_filename)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_link_t/reserved)

#### Initializers

- [init(source: UnsafeMutablePointer<es_file_t>, target_dir: UnsafeMutablePointer<es_file_t>, target_filename: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_link_t/init(source:target_dir:target_filename:reserved:))
- [es_event_readlink_t](/documentation/endpointsecurity/es_event_readlink_t)

#### Inspecting Event Properties

- [var source: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_readlink_t/source)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_readlink_t/reserved)

#### Initializers

- [init(source: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_readlink_t/init(source:reserved:))
- [es_event_unlink_t](/documentation/endpointsecurity/es_event_unlink_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_unlink_t/target)
- [var parent_dir: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_unlink_t/parent_dir)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_unlink_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, parent_dir: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_unlink_t/init(target:parent_dir:reserved:))

### File System Mounting Event Types

- [es_event_mount_t](/documentation/endpointsecurity/es_event_mount_t)

#### Inspecting Event Properties

- [var statfs: UnsafeMutablePointer<statfs>](/documentation/endpointsecurity/es_event_mount_t/statfs)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_mount_t/reserved)

#### Initializers

- [init(statfs: UnsafeMutablePointer<statfs>, disposition: es_mount_disposition_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_mount_t/init(statfs:disposition:reserved:))

#### Instance Properties

- [var disposition: es_mount_disposition_t](/documentation/endpointsecurity/es_event_mount_t/disposition)
- [es_event_unmount_t](/documentation/endpointsecurity/es_event_unmount_t)

#### Inspecting Event Properties

- [var statfs: UnsafeMutablePointer<statfs>](/documentation/endpointsecurity/es_event_unmount_t/statfs)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_unmount_t/reserved)

#### Initializers

- [init(statfs: UnsafeMutablePointer<statfs>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_unmount_t/init(statfs:reserved:))
- [es_event_remount_t](/documentation/endpointsecurity/es_event_remount_t)

#### Inspecting Event Properties

- [var statfs: UnsafeMutablePointer<statfs>](/documentation/endpointsecurity/es_event_remount_t/statfs)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_remount_t/reserved)

#### Initializers

- [init(statfs: UnsafeMutablePointer<statfs>, remount_flags: UInt64, disposition: es_mount_disposition_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_remount_t/init(statfs:remount_flags:disposition:reserved:))

#### Instance Properties

- [var disposition: es_mount_disposition_t](/documentation/endpointsecurity/es_event_remount_t/disposition)
- [var remount_flags: UInt64](/documentation/endpointsecurity/es_event_remount_t/remount_flags)

### Memory Mapping Event Types

- [es_event_mmap_t](/documentation/endpointsecurity/es_event_mmap_t)

#### Inspecting Event Properties

- [var source: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_mmap_t/source)
- [var file_pos: UInt64](/documentation/endpointsecurity/es_event_mmap_t/file_pos)
- [var flags: Int32](/documentation/endpointsecurity/es_event_mmap_t/flags)
- [var max_protection: Int32](/documentation/endpointsecurity/es_event_mmap_t/max_protection)
- [var protection: Int32](/documentation/endpointsecurity/es_event_mmap_t/protection)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_mmap_t/reserved)

#### Initializers

- [init(protection: Int32, max_protection: Int32, flags: Int32, file_pos: UInt64, source: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_mmap_t/init(protection:max_protection:flags:file_pos:source:reserved:))
- [es_event_mprotect_t](/documentation/endpointsecurity/es_event_mprotect_t)

#### Inspecting Event Properties

- [var address: user_addr_t](/documentation/endpointsecurity/es_event_mprotect_t/address)
- [var size: user_size_t](/documentation/endpointsecurity/es_event_mprotect_t/size)
- [var protection: Int32](/documentation/endpointsecurity/es_event_mprotect_t/protection)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_mprotect_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_mprotect_t/init())
- [init(protection: Int32, address: user_addr_t, size: user_size_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_mprotect_t/init(protection:address:size:reserved:))

### Process Event Types

- [es_event_chdir_t](/documentation/endpointsecurity/es_event_chdir_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_chdir_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_chdir_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_chdir_t/init(target:reserved:))
- [es_event_chroot_t](/documentation/endpointsecurity/es_event_chroot_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_chroot_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_chroot_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_file_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_chroot_t/init(target:reserved:))
- [es_event_exec_t](/documentation/endpointsecurity/es_event_exec_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_exec_t/target)
- [es_process_t](/documentation/endpointsecurity/es_process_t)

##### Inspecting the Source Process

- [var audit_token: audit_token_t](/documentation/endpointsecurity/es_process_t/audit_token)
- [var executable: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_process_t/executable)
- [var is_es_client: Bool](/documentation/endpointsecurity/es_process_t/is_es_client)
- [var is_platform_binary: Bool](/documentation/endpointsecurity/es_process_t/is_platform_binary)
- [var start_time: timeval](/documentation/endpointsecurity/es_process_t/start_time)

##### Inspecting Process IDs

- [var ppid: pid_t](/documentation/endpointsecurity/es_process_t/ppid)
- [var original_ppid: pid_t](/documentation/endpointsecurity/es_process_t/original_ppid)
- [var group_id: pid_t](/documentation/endpointsecurity/es_process_t/group_id)
- [var session_id: pid_t](/documentation/endpointsecurity/es_process_t/session_id)
- [var tty: UnsafeMutablePointer<es_file_t>?](/documentation/endpointsecurity/es_process_t/tty)

##### Inspecting Code Signing Properties

- [var codesigning_flags: UInt32](/documentation/endpointsecurity/es_process_t/codesigning_flags)
- [var cdhash: es_cdhash_t](/documentation/endpointsecurity/es_process_t/cdhash)
- [var signing_id: es_string_token_t](/documentation/endpointsecurity/es_process_t/signing_id)
- [var team_id: es_string_token_t](/documentation/endpointsecurity/es_process_t/team_id)

##### Inspecting Audit Tokens

- [var responsible_audit_token: audit_token_t](/documentation/endpointsecurity/es_process_t/responsible_audit_token)
- [var parent_audit_token: audit_token_t](/documentation/endpointsecurity/es_process_t/parent_audit_token)

##### Initializers

- [init(audit_token: audit_token_t, ppid: pid_t, original_ppid: pid_t, group_id: pid_t, session_id: pid_t, codesigning_flags: UInt32, is_platform_binary: Bool, is_es_client: Bool, cdhash: es_cdhash_t, signing_id: es_string_token_t, team_id: es_string_token_t, executable: UnsafeMutablePointer<es_file_t>, tty: UnsafeMutablePointer<es_file_t>?, start_time: timeval, responsible_audit_token: audit_token_t, parent_audit_token: audit_token_t, cs_validation_category: es_cs_validation_category_t)](/documentation/endpointsecurity/es_process_t/init(audit_token:ppid:original_ppid:group_id:session_id:codesigning_flags:is_platform_binary:is_es_client:cdhash:signing_id:team_id:executable:tty:start_time:responsible_audit_token:parent_audit_token:cs_validation_category:))

##### Instance Properties

- [var cs_validation_category: es_cs_validation_category_t](/documentation/endpointsecurity/es_process_t/cs_validation_category)

#### Instance Properties

- [var cwd: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_exec_t/cwd-7pogi)
- [var dyld_exec_path: es_string_token_t](/documentation/endpointsecurity/es_event_exec_t/dyld_exec_path)
- [var image_cpusubtype: cpu_subtype_t](/documentation/endpointsecurity/es_event_exec_t/image_cpusubtype-4h1ft)
- [var image_cputype: cpu_type_t](/documentation/endpointsecurity/es_event_exec_t/image_cputype-9u2jr)
- [var last_fd: Int32](/documentation/endpointsecurity/es_event_exec_t/last_fd-g0rc)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_exec_t/reserved-25qdu)
- [var script: UnsafeMutablePointer<es_file_t>?](/documentation/endpointsecurity/es_event_exec_t/script-19tlj)
- [es_event_fork_t](/documentation/endpointsecurity/es_event_fork_t)

#### Inspecting Event Properties

- [var child: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_fork_t/child)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_fork_t/reserved)

#### Initializers

- [init(child: UnsafeMutablePointer<es_process_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_fork_t/init(child:reserved:))
- [es_event_proc_check_t](/documentation/endpointsecurity/es_event_proc_check_t)

#### Inspecting Event Properties

- [var flavor: Int32](/documentation/endpointsecurity/es_event_proc_check_t/flavor)
- [var target: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_proc_check_t/target)
- [var type: es_proc_check_type_t](/documentation/endpointsecurity/es_event_proc_check_t/type)
- [es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_t)

##### Process Check Result Types

- [var ES_PROC_CHECK_TYPE_DIRTYCONTROL: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_dirtycontrol)
- [var ES_PROC_CHECK_TYPE_LISTPIDS: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_listpids)
- [var ES_PROC_CHECK_TYPE_PIDFDINFO: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_pidfdinfo)
- [var ES_PROC_CHECK_TYPE_PIDFILEPORTINFO: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_pidfileportinfo)
- [var ES_PROC_CHECK_TYPE_PIDINFO: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_pidinfo)
- [var ES_PROC_CHECK_TYPE_PIDRUSAGE: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_pidrusage)
- [var ES_PROC_CHECK_TYPE_SETCONTROL: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_setcontrol)

##### Deprecated Result Types

- [var ES_PROC_CHECK_TYPE_KERNMSGBUF: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_kernmsgbuf)
- [var ES_PROC_CHECK_TYPE_TERMINATE: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_terminate)
- [var ES_PROC_CHECK_TYPE_UDATA_INFO: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_udata_info)

##### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_proc_check_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_proc_check_type_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_proc_check_type_t/rawvalue)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_proc_check_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_proc_check_t/init())
- [init(target: UnsafeMutablePointer<es_process_t>?, type: es_proc_check_type_t, flavor: Int32, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_proc_check_t/init(target:type:flavor:reserved:))
- [es_event_signal_t](/documentation/endpointsecurity/es_event_signal_t)

#### Inspecting Event Properties

- [var sig: Int32](/documentation/endpointsecurity/es_event_signal_t/sig)
- [var target: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_signal_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_signal_t/reserved)

#### Initializers

- [init(sig: Int32, target: UnsafeMutablePointer<es_process_t>, instigator: UnsafeMutablePointer<es_process_t>?, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_signal_t/init(sig:target:instigator:reserved:))

#### Instance Properties

- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_signal_t/instigator)
- [es_event_exit_t](/documentation/endpointsecurity/es_event_exit_t)

#### Inspecting Event Properties

- [var stat: Int32](/documentation/endpointsecurity/es_event_exit_t/stat)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_exit_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_exit_t/init())
- [init(stat: Int32, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_exit_t/init(stat:reserved:))

### Process Event Helper Functions

- [func es_exec_arg(UnsafePointer<es_event_exec_t>, UInt32) -> es_string_token_t](/documentation/endpointsecurity/es_exec_arg(_:_:))
- [func es_exec_arg_count(UnsafePointer<es_event_exec_t>) -> UInt32](/documentation/endpointsecurity/es_exec_arg_count(_:))
- [func es_exec_env(UnsafePointer<es_event_exec_t>, UInt32) -> es_string_token_t](/documentation/endpointsecurity/es_exec_env(_:_:))
- [func es_exec_env_count(UnsafePointer<es_event_exec_t>) -> UInt32](/documentation/endpointsecurity/es_exec_env_count(_:))
- [func es_exec_fd(UnsafePointer<es_event_exec_t>, UInt32) -> UnsafePointer<es_fd_t>](/documentation/endpointsecurity/es_exec_fd(_:_:))
- [func es_exec_fd_count(UnsafePointer<es_event_exec_t>) -> UInt32](/documentation/endpointsecurity/es_exec_fd_count(_:))
- [es_fd_t](/documentation/endpointsecurity/es_fd_t)

#### Inspecting File Descriptor Properties

- [var fd: Int32](/documentation/endpointsecurity/es_fd_t/fd)
- [var fdtype: UInt32](/documentation/endpointsecurity/es_fd_t/fdtype)

#### Initializers

- [init()](/documentation/endpointsecurity/es_fd_t/init())

#### Instance Properties

- [var pipe: es_fd_t.__Unnamed_union___Anonymous_field2.__Unnamed_struct_pipe](/documentation/endpointsecurity/es_fd_t/pipe-1gtm4)

### Interprocess Events

- [es_event_proc_suspend_resume_t](/documentation/endpointsecurity/es_event_proc_suspend_resume_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_proc_suspend_resume_t/target)
- [var type: es_proc_suspend_resume_type_t](/documentation/endpointsecurity/es_event_proc_suspend_resume_t/type)
- [es_proc_suspend_resume_type_t](/documentation/endpointsecurity/es_proc_suspend_resume_type_t)

##### Event Types

- [var ES_PROC_SUSPEND_RESUME_TYPE_SUSPEND: es_proc_suspend_resume_type_t](/documentation/endpointsecurity/es_proc_suspend_resume_type_suspend)
- [var ES_PROC_SUSPEND_RESUME_TYPE_RESUME: es_proc_suspend_resume_type_t](/documentation/endpointsecurity/es_proc_suspend_resume_type_resume)
- [var ES_PROC_SUSPEND_RESUME_TYPE_SHUTDOWN_SOCKETS: es_proc_suspend_resume_type_t](/documentation/endpointsecurity/es_proc_suspend_resume_type_shutdown_sockets)

##### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_proc_suspend_resume_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_proc_suspend_resume_type_t/init(rawvalue:))

##### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_proc_suspend_resume_type_t/rawvalue)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_proc_suspend_resume_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_proc_suspend_resume_t/init())
- [init(target: UnsafeMutablePointer<es_process_t>?, type: es_proc_suspend_resume_type_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_proc_suspend_resume_t/init(target:type:reserved:))
- [es_event_trace_t](/documentation/endpointsecurity/es_event_trace_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_trace_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_trace_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_process_t>, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_trace_t/init(target:reserved:))
- [es_event_remote_thread_create_t](/documentation/endpointsecurity/es_event_remote_thread_create_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_remote_thread_create_t/target)
- [var thread_state: UnsafeMutablePointer<es_thread_state_t>?](/documentation/endpointsecurity/es_event_remote_thread_create_t/thread_state)
- [es_thread_state_t](/documentation/endpointsecurity/es_thread_state_t)

##### Inspecting Thread State

- [var flavor: Int32](/documentation/endpointsecurity/es_thread_state_t/flavor)
- [var state: es_token_t](/documentation/endpointsecurity/es_thread_state_t/state)
- [es_token_t](/documentation/endpointsecurity/es_token_t)

###### Inspecting the Token

- [var data: UnsafePointer<UInt8>!](/documentation/endpointsecurity/es_token_t/data)
- [var size: Int](/documentation/endpointsecurity/es_token_t/size)

###### Initializers

- [init()](/documentation/endpointsecurity/es_token_t/init())
- [init(size: Int, data: UnsafePointer<UInt8>!)](/documentation/endpointsecurity/es_token_t/init(size:data:))

##### Initializers

- [init()](/documentation/endpointsecurity/es_thread_state_t/init())
- [init(flavor: Int32, state: es_token_t)](/documentation/endpointsecurity/es_thread_state_t/init(flavor:state:))
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_remote_thread_create_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_process_t>, thread_state: UnsafeMutablePointer<es_thread_state_t>?, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_remote_thread_create_t/init(target:thread_state:reserved:))

### Task Port Event Types

- [es_event_get_task_t](/documentation/endpointsecurity/es_event_get_task_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_get_task_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_get_task_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_process_t>, type: es_get_task_type_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_get_task_t/init(target:type:reserved:))

#### Instance Properties

- [var type: es_get_task_type_t](/documentation/endpointsecurity/es_event_get_task_t/type)
- [es_event_get_task_read_t](/documentation/endpointsecurity/es_event_get_task_read_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_get_task_read_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_get_task_read_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_process_t>, type: es_get_task_type_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_get_task_read_t/init(target:type:reserved:))

#### Instance Properties

- [var type: es_get_task_type_t](/documentation/endpointsecurity/es_event_get_task_read_t/type)
- [es_event_get_task_inspect_t](/documentation/endpointsecurity/es_event_get_task_inspect_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_get_task_inspect_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_get_task_inspect_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_process_t>, type: es_get_task_type_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_get_task_inspect_t/init(target:type:reserved:))

#### Instance Properties

- [var type: es_get_task_type_t](/documentation/endpointsecurity/es_event_get_task_inspect_t/type)
- [es_event_get_task_name_t](/documentation/endpointsecurity/es_event_get_task_name_t)

#### Inspecting Event Properties

- [var target: UnsafeMutablePointer<es_process_t>](/documentation/endpointsecurity/es_event_get_task_name_t/target)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_get_task_name_t/reserved)

#### Initializers

- [init(target: UnsafeMutablePointer<es_process_t>, type: es_get_task_type_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_get_task_name_t/init(target:type:reserved:))

#### Instance Properties

- [var type: es_get_task_type_t](/documentation/endpointsecurity/es_event_get_task_name_t/type)

### User and Group ID Types

- [es_event_setuid_t](/documentation/endpointsecurity/es_event_setuid_t)

#### Inspecting Event Properties

- [var uid: uid_t](/documentation/endpointsecurity/es_event_setuid_t/uid)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setuid_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_setuid_t/init())
- [init(uid: uid_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setuid_t/init(uid:reserved:))
- [es_event_setgid_t](/documentation/endpointsecurity/es_event_setgid_t)

#### Inspecting Event Properties

- [var gid: uid_t](/documentation/endpointsecurity/es_event_setgid_t/gid)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setgid_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_setgid_t/init())
- [init(gid: uid_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setgid_t/init(gid:reserved:))
- [es_event_seteuid_t](/documentation/endpointsecurity/es_event_seteuid_t)

#### Inspecting Event Properties

- [var euid: uid_t](/documentation/endpointsecurity/es_event_seteuid_t/euid)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_seteuid_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_seteuid_t/init())
- [init(euid: uid_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_seteuid_t/init(euid:reserved:))
- [es_event_setegid_t](/documentation/endpointsecurity/es_event_setegid_t)

#### Inspecting Event Properties

- [var egid: uid_t](/documentation/endpointsecurity/es_event_setegid_t/egid)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setegid_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_setegid_t/init())
- [init(egid: uid_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setegid_t/init(egid:reserved:))
- [es_event_setreuid_t](/documentation/endpointsecurity/es_event_setreuid_t)

#### Inspecting Event Properties

- [var ruid: uid_t](/documentation/endpointsecurity/es_event_setreuid_t/ruid)
- [var euid: uid_t](/documentation/endpointsecurity/es_event_setreuid_t/euid)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setreuid_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_setreuid_t/init())
- [init(ruid: uid_t, euid: uid_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setreuid_t/init(ruid:euid:reserved:))
- [es_event_setregid_t](/documentation/endpointsecurity/es_event_setregid_t)

#### Inspecting Event Properties

- [var rgid: uid_t](/documentation/endpointsecurity/es_event_setregid_t/rgid)
- [var egid: uid_t](/documentation/endpointsecurity/es_event_setregid_t/egid)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_setregid_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_setregid_t/init())
- [init(rgid: uid_t, egid: uid_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_setregid_t/init(rgid:egid:reserved:))

### Code Signing Event Types

- [es_event_cs_invalidated_t](/documentation/endpointsecurity/es_event_cs_invalidated_t)

#### Inspecting Event Properties

- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_cs_invalidated_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_cs_invalidated_t/init())
- [init(reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_cs_invalidated_t/init(reserved:))

### Socket Event Types

- [es_event_uipc_bind_t](/documentation/endpointsecurity/es_event_uipc_bind_t)

#### Inspecting Event Properties

- [var dir: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_uipc_bind_t/dir)
- [var filename: es_string_token_t](/documentation/endpointsecurity/es_event_uipc_bind_t/filename)
- [var mode: mode_t](/documentation/endpointsecurity/es_event_uipc_bind_t/mode)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_uipc_bind_t/reserved)

#### Initializers

- [init(dir: UnsafeMutablePointer<es_file_t>, filename: es_string_token_t, mode: mode_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_uipc_bind_t/init(dir:filename:mode:reserved:))
- [es_event_uipc_connect_t](/documentation/endpointsecurity/es_event_uipc_connect_t)

#### Inspecting Event Properties

- [var file: UnsafeMutablePointer<es_file_t>](/documentation/endpointsecurity/es_event_uipc_connect_t/file)
- [var domain: Int32](/documentation/endpointsecurity/es_event_uipc_connect_t/domain)
- [var type: Int32](/documentation/endpointsecurity/es_event_uipc_connect_t/type)
- [var `protocol`: Int32](/documentation/endpointsecurity/es_event_uipc_connect_t/protocol)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_uipc_connect_t/reserved)

#### Initializers

- [init(file: UnsafeMutablePointer<es_file_t>, domain: Int32, type: Int32, protocol: Int32, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_uipc_connect_t/init(file:domain:type:protocol:reserved:))

### Clock Event Types

- [es_event_settime_t](/documentation/endpointsecurity/es_event_settime_t)

#### Inspecting Event Properties

- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_settime_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_settime_t/init())
- [init(reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_settime_t/init(reserved:))

### Kernel Event Types

- [es_event_iokit_open_t](/documentation/endpointsecurity/es_event_iokit_open_t)

#### Inspecting Event Properties

- [var user_client_class: es_string_token_t](/documentation/endpointsecurity/es_event_iokit_open_t/user_client_class)
- [var user_client_type: UInt32](/documentation/endpointsecurity/es_event_iokit_open_t/user_client_type)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_iokit_open_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_iokit_open_t/init())
- [init(user_client_type: UInt32, user_client_class: es_string_token_t, parent_registry_id: UInt64, parent_path: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_iokit_open_t/init(user_client_type:user_client_class:parent_registry_id:parent_path:reserved:))

#### Instance Properties

- [var parent_path: es_string_token_t](/documentation/endpointsecurity/es_event_iokit_open_t/parent_path)
- [var parent_registry_id: UInt64](/documentation/endpointsecurity/es_event_iokit_open_t/parent_registry_id)
- [es_event_kextload_t](/documentation/endpointsecurity/es_event_kextload_t)

#### Inspecting Event Properties

- [var identifier: es_string_token_t](/documentation/endpointsecurity/es_event_kextload_t/identifier)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_kextload_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_kextload_t/init())
- [init(identifier: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_kextload_t/init(identifier:reserved:))
- [es_event_kextunload_t](/documentation/endpointsecurity/es_event_kextunload_t)

#### Inspecting Event Properties

- [var identifier: es_string_token_t](/documentation/endpointsecurity/es_event_kextunload_t/identifier)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_kextunload_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_kextunload_t/init())
- [init(identifier: es_string_token_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_kextunload_t/init(identifier:reserved:))

### Pseudoterminal Event Types

- [es_event_pty_close_t](/documentation/endpointsecurity/es_event_pty_close_t)

#### Inspecting Event Properties

- [var dev: dev_t](/documentation/endpointsecurity/es_event_pty_close_t/dev)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_pty_close_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_pty_close_t/init())
- [init(dev: dev_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_pty_close_t/init(dev:reserved:))
- [es_event_pty_grant_t](/documentation/endpointsecurity/es_event_pty_grant_t)

#### Inspecting Event Properties

- [var dev: dev_t](/documentation/endpointsecurity/es_event_pty_grant_t/dev)
- [var reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/endpointsecurity/es_event_pty_grant_t/reserved)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_pty_grant_t/init())
- [init(dev: dev_t, reserved: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/endpointsecurity/es_event_pty_grant_t/init(dev:reserved:))

## Entitlements

- [com.apple.developer.endpoint-security.client](/documentation/bundleresources/entitlements/com.apple.developer.endpoint-security.client)

## Reference

- [EndpointSecurity Constants](/documentation/endpointsecurity/endpointsecurity-constants)

### Constants

- [var ES_ADDRESS_TYPE_IPV4: es_address_type_t](/documentation/endpointsecurity/es_address_type_ipv4)
- [var ES_ADDRESS_TYPE_IPV6: es_address_type_t](/documentation/endpointsecurity/es_address_type_ipv6)
- [var ES_ADDRESS_TYPE_NAMED_SOCKET: es_address_type_t](/documentation/endpointsecurity/es_address_type_named_socket)
- [var ES_ADDRESS_TYPE_NONE: es_address_type_t](/documentation/endpointsecurity/es_address_type_none)
- [var ES_AUTHENTICATION_TYPE_AUTO_UNLOCK: es_authentication_type_t](/documentation/endpointsecurity/es_authentication_type_auto_unlock)
- [var ES_AUTHENTICATION_TYPE_LAST: es_authentication_type_t](/documentation/endpointsecurity/es_authentication_type_last)
- [var ES_AUTHENTICATION_TYPE_OD: es_authentication_type_t](/documentation/endpointsecurity/es_authentication_type_od)
- [var ES_AUTHENTICATION_TYPE_TOKEN: es_authentication_type_t](/documentation/endpointsecurity/es_authentication_type_token)
- [var ES_AUTHENTICATION_TYPE_TOUCHID: es_authentication_type_t](/documentation/endpointsecurity/es_authentication_type_touchid)
- [var ES_AUTHORIZATION_RULE_CLASS_ALLOW: es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_rule_class_allow)
- [var ES_AUTHORIZATION_RULE_CLASS_DENY: es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_rule_class_deny)
- [var ES_AUTHORIZATION_RULE_CLASS_INVALID: es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_rule_class_invalid)
- [var ES_AUTHORIZATION_RULE_CLASS_MECHANISM: es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_rule_class_mechanism)
- [var ES_AUTHORIZATION_RULE_CLASS_RULE: es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_rule_class_rule)
- [var ES_AUTHORIZATION_RULE_CLASS_UNKNOWN: es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_rule_class_unknown)
- [var ES_AUTHORIZATION_RULE_CLASS_USER: es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_rule_class_user)
- [var ES_AUTO_UNLOCK_AUTH_PROMPT: es_auto_unlock_type_t](/documentation/endpointsecurity/es_auto_unlock_auth_prompt)
- [var ES_AUTO_UNLOCK_MACHINE_UNLOCK: es_auto_unlock_type_t](/documentation/endpointsecurity/es_auto_unlock_machine_unlock)
- [var ES_BTM_ITEM_TYPE_AGENT: es_btm_item_type_t](/documentation/endpointsecurity/es_btm_item_type_agent)
- [var ES_BTM_ITEM_TYPE_APP: es_btm_item_type_t](/documentation/endpointsecurity/es_btm_item_type_app)
- [var ES_BTM_ITEM_TYPE_DAEMON: es_btm_item_type_t](/documentation/endpointsecurity/es_btm_item_type_daemon)
- [var ES_BTM_ITEM_TYPE_LOGIN_ITEM: es_btm_item_type_t](/documentation/endpointsecurity/es_btm_item_type_login_item)
- [var ES_BTM_ITEM_TYPE_USER_ITEM: es_btm_item_type_t](/documentation/endpointsecurity/es_btm_item_type_user_item)
- [var ES_CLEAR: es_set_or_clear_t](/documentation/endpointsecurity/es_clear)
- [var ES_EVENT_TYPE_NOTIFY_AUTHENTICATION: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_authentication)
- [var ES_EVENT_TYPE_NOTIFY_AUTHORIZATION_JUDGEMENT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_authorization_judgement)
- [var ES_EVENT_TYPE_NOTIFY_AUTHORIZATION_PETITION: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_authorization_petition)
- [var ES_EVENT_TYPE_NOTIFY_BTM_LAUNCH_ITEM_ADD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_btm_launch_item_add)
- [var ES_EVENT_TYPE_NOTIFY_BTM_LAUNCH_ITEM_REMOVE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_btm_launch_item_remove)
- [var ES_EVENT_TYPE_NOTIFY_GATEKEEPER_USER_OVERRIDE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_gatekeeper_user_override)
- [var ES_EVENT_TYPE_NOTIFY_LOGIN_LOGIN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_login_login)
- [var ES_EVENT_TYPE_NOTIFY_LOGIN_LOGOUT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_login_logout)
- [var ES_EVENT_TYPE_NOTIFY_LW_SESSION_LOCK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_lw_session_lock)
- [var ES_EVENT_TYPE_NOTIFY_LW_SESSION_LOGIN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_lw_session_login)
- [var ES_EVENT_TYPE_NOTIFY_LW_SESSION_LOGOUT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_lw_session_logout)
- [var ES_EVENT_TYPE_NOTIFY_LW_SESSION_UNLOCK: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_lw_session_unlock)
- [var ES_EVENT_TYPE_NOTIFY_OD_ATTRIBUTE_SET: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_attribute_set)
- [var ES_EVENT_TYPE_NOTIFY_OD_ATTRIBUTE_VALUE_ADD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_attribute_value_add)
- [var ES_EVENT_TYPE_NOTIFY_OD_ATTRIBUTE_VALUE_REMOVE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_attribute_value_remove)
- [var ES_EVENT_TYPE_NOTIFY_OD_CREATE_GROUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_create_group)
- [var ES_EVENT_TYPE_NOTIFY_OD_CREATE_USER: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_create_user)
- [var ES_EVENT_TYPE_NOTIFY_OD_DELETE_GROUP: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_delete_group)
- [var ES_EVENT_TYPE_NOTIFY_OD_DELETE_USER: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_delete_user)
- [var ES_EVENT_TYPE_NOTIFY_OD_DISABLE_USER: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_disable_user)
- [var ES_EVENT_TYPE_NOTIFY_OD_ENABLE_USER: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_enable_user)
- [var ES_EVENT_TYPE_NOTIFY_OD_GROUP_ADD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_group_add)
- [var ES_EVENT_TYPE_NOTIFY_OD_GROUP_REMOVE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_group_remove)
- [var ES_EVENT_TYPE_NOTIFY_OD_GROUP_SET: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_group_set)
- [var ES_EVENT_TYPE_NOTIFY_OD_MODIFY_PASSWORD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_od_modify_password)
- [var ES_EVENT_TYPE_NOTIFY_OPENSSH_LOGIN: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_openssh_login)
- [var ES_EVENT_TYPE_NOTIFY_OPENSSH_LOGOUT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_openssh_logout)
- [var ES_EVENT_TYPE_NOTIFY_PROFILE_ADD: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_profile_add)
- [var ES_EVENT_TYPE_NOTIFY_PROFILE_REMOVE: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_profile_remove)
- [var ES_EVENT_TYPE_NOTIFY_SCREENSHARING_ATTACH: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_screensharing_attach)
- [var ES_EVENT_TYPE_NOTIFY_SCREENSHARING_DETACH: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_screensharing_detach)
- [var ES_EVENT_TYPE_NOTIFY_SU: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_su)
- [var ES_EVENT_TYPE_NOTIFY_SUDO: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_sudo)
- [var ES_EVENT_TYPE_NOTIFY_XPC_CONNECT: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_xpc_connect)
- [var ES_EVENT_TYPE_NOTIFY_XP_MALWARE_DETECTED: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_xp_malware_detected)
- [var ES_EVENT_TYPE_NOTIFY_XP_MALWARE_REMEDIATED: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_xp_malware_remediated)
- [var ES_GATEKEEPER_USER_OVERRIDE_FILE_TYPE_FILE: es_gatekeeper_user_override_file_type_t](/documentation/endpointsecurity/es_gatekeeper_user_override_file_type_file)
- [var ES_GATEKEEPER_USER_OVERRIDE_FILE_TYPE_PATH: es_gatekeeper_user_override_file_type_t](/documentation/endpointsecurity/es_gatekeeper_user_override_file_type_path)
- [var ES_GET_TASK_TYPE_EXPOSE_TASK: es_get_task_type_t](/documentation/endpointsecurity/es_get_task_type_expose_task)
- [var ES_GET_TASK_TYPE_IDENTITY_TOKEN: es_get_task_type_t](/documentation/endpointsecurity/es_get_task_type_identity_token)
- [var ES_GET_TASK_TYPE_TASK_FOR_PID: es_get_task_type_t](/documentation/endpointsecurity/es_get_task_type_task_for_pid)
- [var ES_MOUNT_DISPOSITION_EXTERNAL: es_mount_disposition_t](/documentation/endpointsecurity/es_mount_disposition_external)
- [var ES_MOUNT_DISPOSITION_INTERNAL: es_mount_disposition_t](/documentation/endpointsecurity/es_mount_disposition_internal)
- [var ES_MOUNT_DISPOSITION_NETWORK: es_mount_disposition_t](/documentation/endpointsecurity/es_mount_disposition_network)
- [var ES_MOUNT_DISPOSITION_NULLFS: es_mount_disposition_t](/documentation/endpointsecurity/es_mount_disposition_nullfs)
- [var ES_MOUNT_DISPOSITION_UNKNOWN: es_mount_disposition_t](/documentation/endpointsecurity/es_mount_disposition_unknown)
- [var ES_MOUNT_DISPOSITION_VIRTUAL: es_mount_disposition_t](/documentation/endpointsecurity/es_mount_disposition_virtual)
- [var ES_MUTE_INVERSION_TYPE_LAST: es_mute_inversion_type_t](/documentation/endpointsecurity/es_mute_inversion_type_last)
- [var ES_MUTE_INVERSION_TYPE_PATH: es_mute_inversion_type_t](/documentation/endpointsecurity/es_mute_inversion_type_path)
- [var ES_MUTE_INVERSION_TYPE_PROCESS: es_mute_inversion_type_t](/documentation/endpointsecurity/es_mute_inversion_type_process)
- [var ES_MUTE_INVERSION_TYPE_TARGET_PATH: es_mute_inversion_type_t](/documentation/endpointsecurity/es_mute_inversion_type_target_path)
- [var ES_MUTE_INVERTED: es_mute_inverted_return_t](/documentation/endpointsecurity/es_mute_inverted)
- [var ES_MUTE_INVERTED_ERROR: es_mute_inverted_return_t](/documentation/endpointsecurity/es_mute_inverted_error)
- [var ES_MUTE_NOT_INVERTED: es_mute_inverted_return_t](/documentation/endpointsecurity/es_mute_not_inverted)
- [var ES_MUTE_PATH_TYPE_TARGET_LITERAL: es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_target_literal)
- [var ES_MUTE_PATH_TYPE_TARGET_PREFIX: es_mute_path_type_t](/documentation/endpointsecurity/es_mute_path_type_target_prefix)
- [var ES_NEW_CLIENT_RESULT_ERR_INTERNAL: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_internal)
- [var ES_NEW_CLIENT_RESULT_ERR_INVALID_ARGUMENT: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_invalid_argument)
- [var ES_NEW_CLIENT_RESULT_ERR_NOT_ENTITLED: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_not_entitled)
- [var ES_NEW_CLIENT_RESULT_ERR_NOT_PERMITTED: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_not_permitted)
- [var ES_NEW_CLIENT_RESULT_ERR_NOT_PRIVILEGED: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_not_privileged)
- [var ES_NEW_CLIENT_RESULT_ERR_TOO_MANY_CLIENTS: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_err_too_many_clients)
- [var ES_NEW_CLIENT_RESULT_SUCCESS: es_new_client_result_t](/documentation/endpointsecurity/es_new_client_result_success)
- [var ES_OD_ACCOUNT_TYPE_COMPUTER: es_od_account_type_t](/documentation/endpointsecurity/es_od_account_type_computer)
- [var ES_OD_ACCOUNT_TYPE_USER: es_od_account_type_t](/documentation/endpointsecurity/es_od_account_type_user)
- [var ES_OD_MEMBER_TYPE_GROUP_UUID: es_od_member_type_t](/documentation/endpointsecurity/es_od_member_type_group_uuid)
- [var ES_OD_MEMBER_TYPE_USER_NAME: es_od_member_type_t](/documentation/endpointsecurity/es_od_member_type_user_name)
- [var ES_OD_MEMBER_TYPE_USER_UUID: es_od_member_type_t](/documentation/endpointsecurity/es_od_member_type_user_uuid)
- [var ES_OD_RECORD_TYPE_GROUP: es_od_record_type_t](/documentation/endpointsecurity/es_od_record_type_group)
- [var ES_OD_RECORD_TYPE_USER: es_od_record_type_t](/documentation/endpointsecurity/es_od_record_type_user)
- [var ES_OPENSSH_AUTH_FAIL_GSSAPI: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_auth_fail_gssapi)
- [var ES_OPENSSH_AUTH_FAIL_HOSTBASED: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_auth_fail_hostbased)
- [var ES_OPENSSH_AUTH_FAIL_KBDINT: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_auth_fail_kbdint)
- [var ES_OPENSSH_AUTH_FAIL_NONE: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_auth_fail_none)
- [var ES_OPENSSH_AUTH_FAIL_PASSWD: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_auth_fail_passwd)
- [var ES_OPENSSH_AUTH_FAIL_PUBKEY: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_auth_fail_pubkey)
- [var ES_OPENSSH_AUTH_SUCCESS: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_auth_success)
- [var ES_OPENSSH_INVALID_USER: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_invalid_user)
- [var ES_OPENSSH_LOGIN_EXCEED_MAXTRIES: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_login_exceed_maxtries)
- [var ES_OPENSSH_LOGIN_ROOT_DENIED: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_login_root_denied)
- [var ES_PROC_CHECK_TYPE_DIRTYCONTROL: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_dirtycontrol)
- [var ES_PROC_CHECK_TYPE_KERNMSGBUF: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_kernmsgbuf)
- [var ES_PROC_CHECK_TYPE_LISTPIDS: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_listpids)
- [var ES_PROC_CHECK_TYPE_PIDFDINFO: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_pidfdinfo)
- [var ES_PROC_CHECK_TYPE_PIDFILEPORTINFO: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_pidfileportinfo)
- [var ES_PROC_CHECK_TYPE_PIDINFO: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_pidinfo)
- [var ES_PROC_CHECK_TYPE_PIDRUSAGE: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_pidrusage)
- [var ES_PROC_CHECK_TYPE_SETCONTROL: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_setcontrol)
- [var ES_PROC_CHECK_TYPE_TERMINATE: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_terminate)
- [var ES_PROC_CHECK_TYPE_UDATA_INFO: es_proc_check_type_t](/documentation/endpointsecurity/es_proc_check_type_udata_info)
- [var ES_PROFILE_SOURCE_INSTALL: es_profile_source_t](/documentation/endpointsecurity/es_profile_source_install)
- [var ES_PROFILE_SOURCE_MANAGED: es_profile_source_t](/documentation/endpointsecurity/es_profile_source_managed)
- [var ES_RETURN_ERROR: es_return_t](/documentation/endpointsecurity/es_return_error)
- [var ES_RETURN_SUCCESS: es_return_t](/documentation/endpointsecurity/es_return_success)
- [var ES_SET: es_set_or_clear_t](/documentation/endpointsecurity/es_set)
- [var ES_SUDO_PLUGIN_TYPE_APPROVAL: es_sudo_plugin_type_t](/documentation/endpointsecurity/es_sudo_plugin_type_approval)
- [var ES_SUDO_PLUGIN_TYPE_AUDIT: es_sudo_plugin_type_t](/documentation/endpointsecurity/es_sudo_plugin_type_audit)
- [var ES_SUDO_PLUGIN_TYPE_FRONT_END: es_sudo_plugin_type_t](/documentation/endpointsecurity/es_sudo_plugin_type_front_end)
- [var ES_SUDO_PLUGIN_TYPE_IO: es_sudo_plugin_type_t](/documentation/endpointsecurity/es_sudo_plugin_type_io)
- [var ES_SUDO_PLUGIN_TYPE_POLICY: es_sudo_plugin_type_t](/documentation/endpointsecurity/es_sudo_plugin_type_policy)
- [var ES_SUDO_PLUGIN_TYPE_UNKNOWN: es_sudo_plugin_type_t](/documentation/endpointsecurity/es_sudo_plugin_type_unknown)
- [var ES_TOUCHID_MODE_IDENTIFICATION: es_touchid_mode_t](/documentation/endpointsecurity/es_touchid_mode_identification)
- [var ES_TOUCHID_MODE_VERIFICATION: es_touchid_mode_t](/documentation/endpointsecurity/es_touchid_mode_verification)
- [var ES_XPC_DOMAIN_TYPE_GUI: es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_gui)
- [var ES_XPC_DOMAIN_TYPE_MANAGER: es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_manager)
- [var ES_XPC_DOMAIN_TYPE_PID: es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_pid)
- [var ES_XPC_DOMAIN_TYPE_PORT: es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_port)
- [var ES_XPC_DOMAIN_TYPE_SESSION: es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_session)
- [var ES_XPC_DOMAIN_TYPE_SYSTEM: es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_system)
- [var ES_XPC_DOMAIN_TYPE_USER: es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_user)
- [var ES_XPC_DOMAIN_TYPE_USER_LOGIN: es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_user_login)
- [EndpointSecurity Data Types](/documentation/endpointsecurity/endpointsecurity-data-types)

### Data Types

- [es_cdhash_t](/documentation/endpointsecurity/es_cdhash_t)
- [es_graphical_session_id_t](/documentation/endpointsecurity/es_graphical_session_id_t)
- [es_sha256_t](/documentation/endpointsecurity/es_sha256_t)
- [EndpointSecurity Functions](/documentation/endpointsecurity/endpointsecurity-functions)

### Functions

- [func es_invert_muting(OpaquePointer, es_mute_inversion_type_t) -> es_return_t](/documentation/endpointsecurity/es_invert_muting(_:_:))
- [func es_muting_inverted(OpaquePointer, es_mute_inversion_type_t) -> es_mute_inverted_return_t](/documentation/endpointsecurity/es_muting_inverted(_:_:))
- [func es_unmute_all_target_paths(OpaquePointer) -> es_return_t](/documentation/endpointsecurity/es_unmute_all_target_paths(_:))
- [EndpointSecurity Structures](/documentation/endpointsecurity/endpointsecurity-structures)

### Structures

- [es_authorization_result_t](/documentation/endpointsecurity/es_authorization_result_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_authorization_result_t/init())
- [init(right_name: es_string_token_t, rule_class: es_authorization_rule_class_t, granted: Bool)](/documentation/endpointsecurity/es_authorization_result_t/init(right_name:rule_class:granted:))

#### Instance Properties

- [var granted: Bool](/documentation/endpointsecurity/es_authorization_result_t/granted)
- [var right_name: es_string_token_t](/documentation/endpointsecurity/es_authorization_result_t/right_name)
- [var rule_class: es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_result_t/rule_class)
- [es_btm_launch_item_t](/documentation/endpointsecurity/es_btm_launch_item_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_btm_launch_item_t/init())
- [init(item_type: es_btm_item_type_t, legacy: Bool, managed: Bool, uid: uid_t, item_url: es_string_token_t, app_url: es_string_token_t)](/documentation/endpointsecurity/es_btm_launch_item_t/init(item_type:legacy:managed:uid:item_url:app_url:))

#### Instance Properties

- [var app_url: es_string_token_t](/documentation/endpointsecurity/es_btm_launch_item_t/app_url)
- [var item_type: es_btm_item_type_t](/documentation/endpointsecurity/es_btm_launch_item_t/item_type)
- [var item_url: es_string_token_t](/documentation/endpointsecurity/es_btm_launch_item_t/item_url)
- [var legacy: Bool](/documentation/endpointsecurity/es_btm_launch_item_t/legacy)
- [var managed: Bool](/documentation/endpointsecurity/es_btm_launch_item_t/managed)
- [var uid: uid_t](/documentation/endpointsecurity/es_btm_launch_item_t/uid)
- [es_event_authentication_auto_unlock_t](/documentation/endpointsecurity/es_event_authentication_auto_unlock_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_authentication_auto_unlock_t/init())
- [init(username: es_string_token_t, type: es_auto_unlock_type_t)](/documentation/endpointsecurity/es_event_authentication_auto_unlock_t/init(username:type:))

#### Instance Properties

- [var type: es_auto_unlock_type_t](/documentation/endpointsecurity/es_event_authentication_auto_unlock_t/type)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_authentication_auto_unlock_t/username)
- [es_event_authentication_od_t](/documentation/endpointsecurity/es_event_authentication_od_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_authentication_od_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, record_type: es_string_token_t, record_name: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_authentication_od_t/init(instigator:record_type:record_name:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_authentication_od_t/db_path)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_authentication_od_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_authentication_od_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_authentication_od_t/node_name)
- [var record_name: es_string_token_t](/documentation/endpointsecurity/es_event_authentication_od_t/record_name)
- [var record_type: es_string_token_t](/documentation/endpointsecurity/es_event_authentication_od_t/record_type)
- [es_event_authentication_t](/documentation/endpointsecurity/es_event_authentication_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_authentication_t/init())
- [init(success: Bool, type: es_authentication_type_t, data: es_event_authentication_t.__Unnamed_union_data)](/documentation/endpointsecurity/es_event_authentication_t/init(success:type:data:))

#### Instance Properties

- [var data: es_event_authentication_t.__Unnamed_union_data](/documentation/endpointsecurity/es_event_authentication_t/data)
- [var success: Bool](/documentation/endpointsecurity/es_event_authentication_t/success)
- [var type: es_authentication_type_t](/documentation/endpointsecurity/es_event_authentication_t/type)
- [es_event_authentication_token_t](/documentation/endpointsecurity/es_event_authentication_token_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_authentication_token_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, pubkey_hash: es_string_token_t, token_id: es_string_token_t, kerberos_principal: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_authentication_token_t/init(instigator:pubkey_hash:token_id:kerberos_principal:instigator_token:))

#### Instance Properties

- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_authentication_token_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_authentication_token_t/instigator_token)
- [var kerberos_principal: es_string_token_t](/documentation/endpointsecurity/es_event_authentication_token_t/kerberos_principal)
- [var pubkey_hash: es_string_token_t](/documentation/endpointsecurity/es_event_authentication_token_t/pubkey_hash)
- [var token_id: es_string_token_t](/documentation/endpointsecurity/es_event_authentication_token_t/token_id)
- [es_event_authentication_touchid_t](/documentation/endpointsecurity/es_event_authentication_touchid_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_authentication_touchid_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, touchid_mode: es_touchid_mode_t, has_uid: Bool, uid: es_event_authentication_touchid_t.__Unnamed_union_uid, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_authentication_touchid_t/init(instigator:touchid_mode:has_uid:uid:instigator_token:))

#### Instance Properties

- [var has_uid: Bool](/documentation/endpointsecurity/es_event_authentication_touchid_t/has_uid)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_authentication_touchid_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_authentication_touchid_t/instigator_token)
- [var touchid_mode: es_touchid_mode_t](/documentation/endpointsecurity/es_event_authentication_touchid_t/touchid_mode)
- [var uid: es_event_authentication_touchid_t.__Unnamed_union_uid](/documentation/endpointsecurity/es_event_authentication_touchid_t/uid)
- [es_event_authorization_judgement_t](/documentation/endpointsecurity/es_event_authorization_judgement_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_authorization_judgement_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, petitioner: UnsafeMutablePointer<es_process_t>?, return_code: Int32, result_count: Int, results: UnsafeMutablePointer<es_authorization_result_t>?, instigator_token: audit_token_t, petitioner_token: audit_token_t)](/documentation/endpointsecurity/es_event_authorization_judgement_t/init(instigator:petitioner:return_code:result_count:results:instigator_token:petitioner_token:))

#### Instance Properties

- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_authorization_judgement_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_authorization_judgement_t/instigator_token)
- [var petitioner: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_authorization_judgement_t/petitioner)
- [var petitioner_token: audit_token_t](/documentation/endpointsecurity/es_event_authorization_judgement_t/petitioner_token)
- [var result_count: Int](/documentation/endpointsecurity/es_event_authorization_judgement_t/result_count)
- [var results: UnsafeMutablePointer<es_authorization_result_t>?](/documentation/endpointsecurity/es_event_authorization_judgement_t/results)
- [var return_code: Int32](/documentation/endpointsecurity/es_event_authorization_judgement_t/return_code)
- [es_event_authorization_petition_t](/documentation/endpointsecurity/es_event_authorization_petition_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_authorization_petition_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, petitioner: UnsafeMutablePointer<es_process_t>?, flags: UInt32, right_count: Int, rights: UnsafeMutablePointer<es_string_token_t>?, instigator_token: audit_token_t, petitioner_token: audit_token_t)](/documentation/endpointsecurity/es_event_authorization_petition_t/init(instigator:petitioner:flags:right_count:rights:instigator_token:petitioner_token:))

#### Instance Properties

- [var flags: UInt32](/documentation/endpointsecurity/es_event_authorization_petition_t/flags)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_authorization_petition_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_authorization_petition_t/instigator_token)
- [var petitioner: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_authorization_petition_t/petitioner)
- [var petitioner_token: audit_token_t](/documentation/endpointsecurity/es_event_authorization_petition_t/petitioner_token)
- [var right_count: Int](/documentation/endpointsecurity/es_event_authorization_petition_t/right_count)
- [var rights: UnsafeMutablePointer<es_string_token_t>?](/documentation/endpointsecurity/es_event_authorization_petition_t/rights)
- [es_event_btm_launch_item_add_t](/documentation/endpointsecurity/es_event_btm_launch_item_add_t)

#### Initializers

- [init(instigator: UnsafeMutablePointer<es_process_t>?, app: UnsafeMutablePointer<es_process_t>?, item: UnsafeMutablePointer<es_btm_launch_item_t>, executable_path: es_string_token_t, instigator_token: UnsafeMutablePointer<audit_token_t>?, app_token: UnsafeMutablePointer<audit_token_t>?)](/documentation/endpointsecurity/es_event_btm_launch_item_add_t/init(instigator:app:item:executable_path:instigator_token:app_token:))

#### Instance Properties

- [var app: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_btm_launch_item_add_t/app)
- [var app_token: UnsafeMutablePointer<audit_token_t>?](/documentation/endpointsecurity/es_event_btm_launch_item_add_t/app_token)
- [var executable_path: es_string_token_t](/documentation/endpointsecurity/es_event_btm_launch_item_add_t/executable_path)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_btm_launch_item_add_t/instigator)
- [var instigator_token: UnsafeMutablePointer<audit_token_t>?](/documentation/endpointsecurity/es_event_btm_launch_item_add_t/instigator_token)
- [var item: UnsafeMutablePointer<es_btm_launch_item_t>](/documentation/endpointsecurity/es_event_btm_launch_item_add_t/item)
- [es_event_btm_launch_item_remove_t](/documentation/endpointsecurity/es_event_btm_launch_item_remove_t)

#### Initializers

- [init(instigator: UnsafeMutablePointer<es_process_t>?, app: UnsafeMutablePointer<es_process_t>?, item: UnsafeMutablePointer<es_btm_launch_item_t>, instigator_token: UnsafeMutablePointer<audit_token_t>?, app_token: UnsafeMutablePointer<audit_token_t>?)](/documentation/endpointsecurity/es_event_btm_launch_item_remove_t/init(instigator:app:item:instigator_token:app_token:))

#### Instance Properties

- [var app: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_btm_launch_item_remove_t/app)
- [var app_token: UnsafeMutablePointer<audit_token_t>?](/documentation/endpointsecurity/es_event_btm_launch_item_remove_t/app_token)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_btm_launch_item_remove_t/instigator)
- [var instigator_token: UnsafeMutablePointer<audit_token_t>?](/documentation/endpointsecurity/es_event_btm_launch_item_remove_t/instigator_token)
- [var item: UnsafeMutablePointer<es_btm_launch_item_t>](/documentation/endpointsecurity/es_event_btm_launch_item_remove_t/item)
- [es_event_gatekeeper_user_override_t](/documentation/endpointsecurity/es_event_gatekeeper_user_override_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_gatekeeper_user_override_t/init())
- [init(file_type: es_gatekeeper_user_override_file_type_t, file: es_event_gatekeeper_user_override_t.__Unnamed_union_file, sha256: UnsafeMutablePointer<es_sha256_t>?, signing_info: UnsafeMutablePointer<es_signed_file_info_t>?)](/documentation/endpointsecurity/es_event_gatekeeper_user_override_t/init(file_type:file:sha256:signing_info:))

#### Instance Properties

- [var file: es_event_gatekeeper_user_override_t.__Unnamed_union_file](/documentation/endpointsecurity/es_event_gatekeeper_user_override_t/file)
- [var file_type: es_gatekeeper_user_override_file_type_t](/documentation/endpointsecurity/es_event_gatekeeper_user_override_t/file_type)
- [var sha256: UnsafeMutablePointer<es_sha256_t>?](/documentation/endpointsecurity/es_event_gatekeeper_user_override_t/sha256)
- [var signing_info: UnsafeMutablePointer<es_signed_file_info_t>?](/documentation/endpointsecurity/es_event_gatekeeper_user_override_t/signing_info)
- [es_event_login_login_t](/documentation/endpointsecurity/es_event_login_login_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_login_login_t/init())
- [init(success: Bool, failure_message: es_string_token_t, username: es_string_token_t, has_uid: Bool, uid: es_event_login_login_t.__Unnamed_union_uid)](/documentation/endpointsecurity/es_event_login_login_t/init(success:failure_message:username:has_uid:uid:))

#### Instance Properties

- [var failure_message: es_string_token_t](/documentation/endpointsecurity/es_event_login_login_t/failure_message)
- [var has_uid: Bool](/documentation/endpointsecurity/es_event_login_login_t/has_uid)
- [var success: Bool](/documentation/endpointsecurity/es_event_login_login_t/success)
- [var uid: es_event_login_login_t.__Unnamed_union_uid](/documentation/endpointsecurity/es_event_login_login_t/uid)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_login_login_t/username)
- [es_event_login_logout_t](/documentation/endpointsecurity/es_event_login_logout_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_login_logout_t/init())
- [init(username: es_string_token_t, uid: uid_t)](/documentation/endpointsecurity/es_event_login_logout_t/init(username:uid:))

#### Instance Properties

- [var uid: uid_t](/documentation/endpointsecurity/es_event_login_logout_t/uid)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_login_logout_t/username)
- [es_event_lw_session_lock_t](/documentation/endpointsecurity/es_event_lw_session_lock_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_lw_session_lock_t/init())
- [init(username: es_string_token_t, graphical_session_id: es_graphical_session_id_t)](/documentation/endpointsecurity/es_event_lw_session_lock_t/init(username:graphical_session_id:))

#### Instance Properties

- [var graphical_session_id: es_graphical_session_id_t](/documentation/endpointsecurity/es_event_lw_session_lock_t/graphical_session_id)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_lw_session_lock_t/username)
- [es_event_lw_session_login_t](/documentation/endpointsecurity/es_event_lw_session_login_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_lw_session_login_t/init())
- [init(username: es_string_token_t, graphical_session_id: es_graphical_session_id_t)](/documentation/endpointsecurity/es_event_lw_session_login_t/init(username:graphical_session_id:))

#### Instance Properties

- [var graphical_session_id: es_graphical_session_id_t](/documentation/endpointsecurity/es_event_lw_session_login_t/graphical_session_id)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_lw_session_login_t/username)
- [es_event_lw_session_logout_t](/documentation/endpointsecurity/es_event_lw_session_logout_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_lw_session_logout_t/init())
- [init(username: es_string_token_t, graphical_session_id: es_graphical_session_id_t)](/documentation/endpointsecurity/es_event_lw_session_logout_t/init(username:graphical_session_id:))

#### Instance Properties

- [var graphical_session_id: es_graphical_session_id_t](/documentation/endpointsecurity/es_event_lw_session_logout_t/graphical_session_id)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_lw_session_logout_t/username)
- [es_event_lw_session_unlock_t](/documentation/endpointsecurity/es_event_lw_session_unlock_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_lw_session_unlock_t/init())
- [init(username: es_string_token_t, graphical_session_id: es_graphical_session_id_t)](/documentation/endpointsecurity/es_event_lw_session_unlock_t/init(username:graphical_session_id:))

#### Instance Properties

- [var graphical_session_id: es_graphical_session_id_t](/documentation/endpointsecurity/es_event_lw_session_unlock_t/graphical_session_id)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_lw_session_unlock_t/username)
- [es_event_od_attribute_set_t](/documentation/endpointsecurity/es_event_od_attribute_set_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_attribute_set_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, record_type: es_od_record_type_t, record_name: es_string_token_t, attribute_name: es_string_token_t, attribute_value_count: Int, attribute_values: UnsafeMutablePointer<es_string_token_t>?, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_attribute_set_t/init(instigator:error_code:record_type:record_name:attribute_name:attribute_value_count:attribute_values:node_name:db_path:instigator_token:))

#### Instance Properties

- [var attribute_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_set_t/attribute_name)
- [var attribute_value_count: Int](/documentation/endpointsecurity/es_event_od_attribute_set_t/attribute_value_count)
- [var attribute_values: UnsafeMutablePointer<es_string_token_t>?](/documentation/endpointsecurity/es_event_od_attribute_set_t/attribute_values)
- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_set_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_attribute_set_t/error_code)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_attribute_set_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_attribute_set_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_set_t/node_name)
- [var record_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_set_t/record_name)
- [var record_type: es_od_record_type_t](/documentation/endpointsecurity/es_event_od_attribute_set_t/record_type)
- [es_event_od_attribute_value_add_t](/documentation/endpointsecurity/es_event_od_attribute_value_add_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, record_type: es_od_record_type_t, record_name: es_string_token_t, attribute_name: es_string_token_t, attribute_value: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/init(instigator:error_code:record_type:record_name:attribute_name:attribute_value:node_name:db_path:instigator_token:))

#### Instance Properties

- [var attribute_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/attribute_name)
- [var attribute_value: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/attribute_value)
- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/error_code)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/node_name)
- [var record_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/record_name)
- [var record_type: es_od_record_type_t](/documentation/endpointsecurity/es_event_od_attribute_value_add_t/record_type)
- [es_event_od_attribute_value_remove_t](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, record_type: es_od_record_type_t, record_name: es_string_token_t, attribute_name: es_string_token_t, attribute_value: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/init(instigator:error_code:record_type:record_name:attribute_name:attribute_value:node_name:db_path:instigator_token:))

#### Instance Properties

- [var attribute_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/attribute_name)
- [var attribute_value: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/attribute_value)
- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/error_code)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/node_name)
- [var record_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/record_name)
- [var record_type: es_od_record_type_t](/documentation/endpointsecurity/es_event_od_attribute_value_remove_t/record_type)
- [es_event_od_create_group_t](/documentation/endpointsecurity/es_event_od_create_group_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_create_group_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, group_name: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_create_group_t/init(instigator:error_code:group_name:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_create_group_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_create_group_t/error_code)
- [var group_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_create_group_t/group_name)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_create_group_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_create_group_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_create_group_t/node_name)
- [es_event_od_create_user_t](/documentation/endpointsecurity/es_event_od_create_user_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_create_user_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, user_name: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_create_user_t/init(instigator:error_code:user_name:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_create_user_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_create_user_t/error_code)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_create_user_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_create_user_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_create_user_t/node_name)
- [var user_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_create_user_t/user_name)
- [es_event_od_delete_group_t](/documentation/endpointsecurity/es_event_od_delete_group_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_delete_group_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, group_name: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_delete_group_t/init(instigator:error_code:group_name:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_delete_group_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_delete_group_t/error_code)
- [var group_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_delete_group_t/group_name)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_delete_group_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_delete_group_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_delete_group_t/node_name)
- [es_event_od_delete_user_t](/documentation/endpointsecurity/es_event_od_delete_user_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_delete_user_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, user_name: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_delete_user_t/init(instigator:error_code:user_name:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_delete_user_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_delete_user_t/error_code)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_delete_user_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_delete_user_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_delete_user_t/node_name)
- [var user_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_delete_user_t/user_name)
- [es_event_od_disable_user_t](/documentation/endpointsecurity/es_event_od_disable_user_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_disable_user_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, user_name: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_disable_user_t/init(instigator:error_code:user_name:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_disable_user_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_disable_user_t/error_code)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_disable_user_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_disable_user_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_disable_user_t/node_name)
- [var user_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_disable_user_t/user_name)
- [es_event_od_enable_user_t](/documentation/endpointsecurity/es_event_od_enable_user_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_enable_user_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, user_name: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_enable_user_t/init(instigator:error_code:user_name:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_enable_user_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_enable_user_t/error_code)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_enable_user_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_enable_user_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_enable_user_t/node_name)
- [var user_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_enable_user_t/user_name)
- [es_event_od_group_add_t](/documentation/endpointsecurity/es_event_od_group_add_t)

#### Initializers

- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, group_name: es_string_token_t, member: UnsafeMutablePointer<es_od_member_id_t>, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_group_add_t/init(instigator:error_code:group_name:member:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_add_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_group_add_t/error_code)
- [var group_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_add_t/group_name)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_group_add_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_group_add_t/instigator_token)
- [var member: UnsafeMutablePointer<es_od_member_id_t>](/documentation/endpointsecurity/es_event_od_group_add_t/member)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_add_t/node_name)
- [es_event_od_group_remove_t](/documentation/endpointsecurity/es_event_od_group_remove_t)

#### Initializers

- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, group_name: es_string_token_t, member: UnsafeMutablePointer<es_od_member_id_t>, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_group_remove_t/init(instigator:error_code:group_name:member:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_remove_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_group_remove_t/error_code)
- [var group_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_remove_t/group_name)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_group_remove_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_group_remove_t/instigator_token)
- [var member: UnsafeMutablePointer<es_od_member_id_t>](/documentation/endpointsecurity/es_event_od_group_remove_t/member)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_remove_t/node_name)
- [es_event_od_group_set_t](/documentation/endpointsecurity/es_event_od_group_set_t)

#### Initializers

- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, group_name: es_string_token_t, members: UnsafeMutablePointer<es_od_member_id_array_t>, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_group_set_t/init(instigator:error_code:group_name:members:node_name:db_path:instigator_token:))

#### Instance Properties

- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_set_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_group_set_t/error_code)
- [var group_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_set_t/group_name)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_group_set_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_group_set_t/instigator_token)
- [var members: UnsafeMutablePointer<es_od_member_id_array_t>](/documentation/endpointsecurity/es_event_od_group_set_t/members)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_group_set_t/node_name)
- [es_event_od_modify_password_t](/documentation/endpointsecurity/es_event_od_modify_password_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_od_modify_password_t/init())
- [init(instigator: UnsafeMutablePointer<es_process_t>?, error_code: Int32, account_type: es_od_account_type_t, account_name: es_string_token_t, node_name: es_string_token_t, db_path: es_string_token_t, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_od_modify_password_t/init(instigator:error_code:account_type:account_name:node_name:db_path:instigator_token:))

#### Instance Properties

- [var account_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_modify_password_t/account_name)
- [var account_type: es_od_account_type_t](/documentation/endpointsecurity/es_event_od_modify_password_t/account_type)
- [var db_path: es_string_token_t](/documentation/endpointsecurity/es_event_od_modify_password_t/db_path)
- [var error_code: Int32](/documentation/endpointsecurity/es_event_od_modify_password_t/error_code)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_od_modify_password_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_od_modify_password_t/instigator_token)
- [var node_name: es_string_token_t](/documentation/endpointsecurity/es_event_od_modify_password_t/node_name)
- [es_event_openssh_login_t](/documentation/endpointsecurity/es_event_openssh_login_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_openssh_login_t/init())
- [init(success: Bool, result_type: es_openssh_login_result_type_t, source_address_type: es_address_type_t, source_address: es_string_token_t, username: es_string_token_t, has_uid: Bool, uid: es_event_openssh_login_t.__Unnamed_union_uid)](/documentation/endpointsecurity/es_event_openssh_login_t/init(success:result_type:source_address_type:source_address:username:has_uid:uid:))

#### Instance Properties

- [var has_uid: Bool](/documentation/endpointsecurity/es_event_openssh_login_t/has_uid)
- [var result_type: es_openssh_login_result_type_t](/documentation/endpointsecurity/es_event_openssh_login_t/result_type)
- [var source_address: es_string_token_t](/documentation/endpointsecurity/es_event_openssh_login_t/source_address)
- [var source_address_type: es_address_type_t](/documentation/endpointsecurity/es_event_openssh_login_t/source_address_type)
- [var success: Bool](/documentation/endpointsecurity/es_event_openssh_login_t/success)
- [var uid: es_event_openssh_login_t.__Unnamed_union_uid](/documentation/endpointsecurity/es_event_openssh_login_t/uid)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_openssh_login_t/username)
- [es_event_openssh_logout_t](/documentation/endpointsecurity/es_event_openssh_logout_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_openssh_logout_t/init())
- [init(source_address_type: es_address_type_t, source_address: es_string_token_t, username: es_string_token_t, uid: uid_t)](/documentation/endpointsecurity/es_event_openssh_logout_t/init(source_address_type:source_address:username:uid:))

#### Instance Properties

- [var source_address: es_string_token_t](/documentation/endpointsecurity/es_event_openssh_logout_t/source_address)
- [var source_address_type: es_address_type_t](/documentation/endpointsecurity/es_event_openssh_logout_t/source_address_type)
- [var uid: uid_t](/documentation/endpointsecurity/es_event_openssh_logout_t/uid)
- [var username: es_string_token_t](/documentation/endpointsecurity/es_event_openssh_logout_t/username)
- [es_event_profile_add_t](/documentation/endpointsecurity/es_event_profile_add_t)

#### Initializers

- [init(instigator: UnsafeMutablePointer<es_process_t>?, is_update: Bool, profile: UnsafeMutablePointer<es_profile_t>, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_profile_add_t/init(instigator:is_update:profile:instigator_token:))

#### Instance Properties

- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_profile_add_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_profile_add_t/instigator_token)
- [var is_update: Bool](/documentation/endpointsecurity/es_event_profile_add_t/is_update)
- [var profile: UnsafeMutablePointer<es_profile_t>](/documentation/endpointsecurity/es_event_profile_add_t/profile)
- [es_event_profile_remove_t](/documentation/endpointsecurity/es_event_profile_remove_t)

#### Initializers

- [init(instigator: UnsafeMutablePointer<es_process_t>?, profile: UnsafeMutablePointer<es_profile_t>, instigator_token: audit_token_t)](/documentation/endpointsecurity/es_event_profile_remove_t/init(instigator:profile:instigator_token:))

#### Instance Properties

- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_profile_remove_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_profile_remove_t/instigator_token)
- [var profile: UnsafeMutablePointer<es_profile_t>](/documentation/endpointsecurity/es_event_profile_remove_t/profile)
- [es_event_screensharing_attach_t](/documentation/endpointsecurity/es_event_screensharing_attach_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_screensharing_attach_t/init())
- [init(success: Bool, source_address_type: es_address_type_t, source_address: es_string_token_t, viewer_appleid: es_string_token_t, authentication_type: es_string_token_t, authentication_username: es_string_token_t, session_username: es_string_token_t, existing_session: Bool, graphical_session_id: es_graphical_session_id_t)](/documentation/endpointsecurity/es_event_screensharing_attach_t/init(success:source_address_type:source_address:viewer_appleid:authentication_type:authentication_username:session_username:existing_session:graphical_session_id:))

#### Instance Properties

- [var authentication_type: es_string_token_t](/documentation/endpointsecurity/es_event_screensharing_attach_t/authentication_type)
- [var authentication_username: es_string_token_t](/documentation/endpointsecurity/es_event_screensharing_attach_t/authentication_username)
- [var existing_session: Bool](/documentation/endpointsecurity/es_event_screensharing_attach_t/existing_session)
- [var graphical_session_id: es_graphical_session_id_t](/documentation/endpointsecurity/es_event_screensharing_attach_t/graphical_session_id)
- [var session_username: es_string_token_t](/documentation/endpointsecurity/es_event_screensharing_attach_t/session_username)
- [var source_address: es_string_token_t](/documentation/endpointsecurity/es_event_screensharing_attach_t/source_address)
- [var source_address_type: es_address_type_t](/documentation/endpointsecurity/es_event_screensharing_attach_t/source_address_type)
- [var success: Bool](/documentation/endpointsecurity/es_event_screensharing_attach_t/success)
- [var viewer_appleid: es_string_token_t](/documentation/endpointsecurity/es_event_screensharing_attach_t/viewer_appleid)
- [es_event_screensharing_detach_t](/documentation/endpointsecurity/es_event_screensharing_detach_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_screensharing_detach_t/init())
- [init(source_address_type: es_address_type_t, source_address: es_string_token_t, viewer_appleid: es_string_token_t, graphical_session_id: es_graphical_session_id_t)](/documentation/endpointsecurity/es_event_screensharing_detach_t/init(source_address_type:source_address:viewer_appleid:graphical_session_id:))

#### Instance Properties

- [var graphical_session_id: es_graphical_session_id_t](/documentation/endpointsecurity/es_event_screensharing_detach_t/graphical_session_id)
- [var source_address: es_string_token_t](/documentation/endpointsecurity/es_event_screensharing_detach_t/source_address)
- [var source_address_type: es_address_type_t](/documentation/endpointsecurity/es_event_screensharing_detach_t/source_address_type)
- [var viewer_appleid: es_string_token_t](/documentation/endpointsecurity/es_event_screensharing_detach_t/viewer_appleid)
- [es_event_su_t](/documentation/endpointsecurity/es_event_su_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_su_t/init())
- [init(success: Bool, failure_message: es_string_token_t, from_uid: uid_t, from_username: es_string_token_t, has_to_uid: Bool, to_uid: es_event_su_t.__Unnamed_union_to_uid, to_username: es_string_token_t, shell: es_string_token_t, argc: Int, argv: UnsafeMutablePointer<es_string_token_t>?, env_count: Int, env: UnsafeMutablePointer<es_string_token_t>?)](/documentation/endpointsecurity/es_event_su_t/init(success:failure_message:from_uid:from_username:has_to_uid:to_uid:to_username:shell:argc:argv:env_count:env:))

#### Instance Properties

- [var argc: Int](/documentation/endpointsecurity/es_event_su_t/argc)
- [var argv: UnsafeMutablePointer<es_string_token_t>?](/documentation/endpointsecurity/es_event_su_t/argv)
- [var env: UnsafeMutablePointer<es_string_token_t>?](/documentation/endpointsecurity/es_event_su_t/env)
- [var env_count: Int](/documentation/endpointsecurity/es_event_su_t/env_count)
- [var failure_message: es_string_token_t](/documentation/endpointsecurity/es_event_su_t/failure_message)
- [var from_uid: uid_t](/documentation/endpointsecurity/es_event_su_t/from_uid)
- [var from_username: es_string_token_t](/documentation/endpointsecurity/es_event_su_t/from_username)
- [var has_to_uid: Bool](/documentation/endpointsecurity/es_event_su_t/has_to_uid)
- [var shell: es_string_token_t](/documentation/endpointsecurity/es_event_su_t/shell)
- [var success: Bool](/documentation/endpointsecurity/es_event_su_t/success)
- [var to_uid: es_event_su_t.__Unnamed_union_to_uid](/documentation/endpointsecurity/es_event_su_t/to_uid)
- [var to_username: es_string_token_t](/documentation/endpointsecurity/es_event_su_t/to_username)
- [es_event_sudo_t](/documentation/endpointsecurity/es_event_sudo_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_sudo_t/init())
- [init(success: Bool, reject_info: UnsafeMutablePointer<es_sudo_reject_info_t>?, has_from_uid: Bool, from_uid: es_event_sudo_t.__Unnamed_union_from_uid, from_username: es_string_token_t, has_to_uid: Bool, to_uid: es_event_sudo_t.__Unnamed_union_to_uid, to_username: es_string_token_t, command: es_string_token_t)](/documentation/endpointsecurity/es_event_sudo_t/init(success:reject_info:has_from_uid:from_uid:from_username:has_to_uid:to_uid:to_username:command:))

#### Instance Properties

- [var command: es_string_token_t](/documentation/endpointsecurity/es_event_sudo_t/command)
- [var from_uid: es_event_sudo_t.__Unnamed_union_from_uid](/documentation/endpointsecurity/es_event_sudo_t/from_uid)
- [var from_username: es_string_token_t](/documentation/endpointsecurity/es_event_sudo_t/from_username)
- [var has_from_uid: Bool](/documentation/endpointsecurity/es_event_sudo_t/has_from_uid)
- [var has_to_uid: Bool](/documentation/endpointsecurity/es_event_sudo_t/has_to_uid)
- [var reject_info: UnsafeMutablePointer<es_sudo_reject_info_t>?](/documentation/endpointsecurity/es_event_sudo_t/reject_info)
- [var success: Bool](/documentation/endpointsecurity/es_event_sudo_t/success)
- [var to_uid: es_event_sudo_t.__Unnamed_union_to_uid](/documentation/endpointsecurity/es_event_sudo_t/to_uid)
- [var to_username: es_string_token_t](/documentation/endpointsecurity/es_event_sudo_t/to_username)
- [es_event_xp_malware_detected_t](/documentation/endpointsecurity/es_event_xp_malware_detected_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_xp_malware_detected_t/init())
- [init(signature_version: es_string_token_t, malware_identifier: es_string_token_t, incident_identifier: es_string_token_t, detected_path: es_string_token_t, detected_executable: es_string_token_t)](/documentation/endpointsecurity/es_event_xp_malware_detected_t/init(signature_version:malware_identifier:incident_identifier:detected_path:detected_executable:))

#### Instance Properties

- [var detected_executable: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_detected_t/detected_executable)
- [var detected_path: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_detected_t/detected_path)
- [var incident_identifier: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_detected_t/incident_identifier)
- [var malware_identifier: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_detected_t/malware_identifier)
- [var signature_version: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_detected_t/signature_version)
- [es_event_xp_malware_remediated_t](/documentation/endpointsecurity/es_event_xp_malware_remediated_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/init())
- [init(signature_version: es_string_token_t, malware_identifier: es_string_token_t, incident_identifier: es_string_token_t, action_type: es_string_token_t, success: Bool, result_description: es_string_token_t, remediated_path: es_string_token_t, remediated_process_audit_token: UnsafeMutablePointer<audit_token_t>?)](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/init(signature_version:malware_identifier:incident_identifier:action_type:success:result_description:remediated_path:remediated_process_audit_token:))

#### Instance Properties

- [var action_type: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/action_type)
- [var incident_identifier: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/incident_identifier)
- [var malware_identifier: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/malware_identifier)
- [var remediated_path: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/remediated_path)
- [var remediated_process_audit_token: UnsafeMutablePointer<audit_token_t>?](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/remediated_process_audit_token)
- [var result_description: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/result_description)
- [var signature_version: es_string_token_t](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/signature_version)
- [var success: Bool](/documentation/endpointsecurity/es_event_xp_malware_remediated_t/success)
- [es_event_xpc_connect_t](/documentation/endpointsecurity/es_event_xpc_connect_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_event_xpc_connect_t/init())
- [init(service_name: es_string_token_t, service_domain_type: es_xpc_domain_type_t)](/documentation/endpointsecurity/es_event_xpc_connect_t/init(service_name:service_domain_type:))

#### Instance Properties

- [var service_domain_type: es_xpc_domain_type_t](/documentation/endpointsecurity/es_event_xpc_connect_t/service_domain_type)
- [var service_name: es_string_token_t](/documentation/endpointsecurity/es_event_xpc_connect_t/service_name)
- [es_od_member_id_array_t](/documentation/endpointsecurity/es_od_member_id_array_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_od_member_id_array_t/init())
- [init(member_type: es_od_member_type_t, member_count: Int, member_array: es_od_member_id_array_t.__Unnamed_union_member_array)](/documentation/endpointsecurity/es_od_member_id_array_t/init(member_type:member_count:member_array:))

#### Instance Properties

- [var member_array: es_od_member_id_array_t.__Unnamed_union_member_array](/documentation/endpointsecurity/es_od_member_id_array_t/member_array)
- [var member_count: Int](/documentation/endpointsecurity/es_od_member_id_array_t/member_count)
- [var member_type: es_od_member_type_t](/documentation/endpointsecurity/es_od_member_id_array_t/member_type)
- [es_od_member_id_t](/documentation/endpointsecurity/es_od_member_id_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_od_member_id_t/init())
- [init(member_type: es_od_member_type_t, member_value: es_od_member_id_t.__Unnamed_union_member_value)](/documentation/endpointsecurity/es_od_member_id_t/init(member_type:member_value:))

#### Instance Properties

- [var member_type: es_od_member_type_t](/documentation/endpointsecurity/es_od_member_id_t/member_type)
- [var member_value: es_od_member_id_t.__Unnamed_union_member_value](/documentation/endpointsecurity/es_od_member_id_t/member_value)
- [es_profile_t](/documentation/endpointsecurity/es_profile_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_profile_t/init())
- [init(identifier: es_string_token_t, uuid: es_string_token_t, install_source: es_profile_source_t, organization: es_string_token_t, display_name: es_string_token_t, scope: es_string_token_t)](/documentation/endpointsecurity/es_profile_t/init(identifier:uuid:install_source:organization:display_name:scope:))

#### Instance Properties

- [var display_name: es_string_token_t](/documentation/endpointsecurity/es_profile_t/display_name)
- [var identifier: es_string_token_t](/documentation/endpointsecurity/es_profile_t/identifier)
- [var install_source: es_profile_source_t](/documentation/endpointsecurity/es_profile_t/install_source)
- [var organization: es_string_token_t](/documentation/endpointsecurity/es_profile_t/organization)
- [var scope: es_string_token_t](/documentation/endpointsecurity/es_profile_t/scope)
- [var uuid: es_string_token_t](/documentation/endpointsecurity/es_profile_t/uuid)
- [es_signed_file_info_t](/documentation/endpointsecurity/es_signed_file_info_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_signed_file_info_t/init())
- [init(cdhash: es_cdhash_t, signing_id: es_string_token_t, team_id: es_string_token_t)](/documentation/endpointsecurity/es_signed_file_info_t/init(cdhash:signing_id:team_id:))

#### Instance Properties

- [var cdhash: es_cdhash_t](/documentation/endpointsecurity/es_signed_file_info_t/cdhash)
- [var signing_id: es_string_token_t](/documentation/endpointsecurity/es_signed_file_info_t/signing_id)
- [var team_id: es_string_token_t](/documentation/endpointsecurity/es_signed_file_info_t/team_id)
- [es_sudo_reject_info_t](/documentation/endpointsecurity/es_sudo_reject_info_t)

#### Initializers

- [init()](/documentation/endpointsecurity/es_sudo_reject_info_t/init())
- [init(plugin_name: es_string_token_t, plugin_type: es_sudo_plugin_type_t, failure_message: es_string_token_t)](/documentation/endpointsecurity/es_sudo_reject_info_t/init(plugin_name:plugin_type:failure_message:))

#### Instance Properties

- [var failure_message: es_string_token_t](/documentation/endpointsecurity/es_sudo_reject_info_t/failure_message)
- [var plugin_name: es_string_token_t](/documentation/endpointsecurity/es_sudo_reject_info_t/plugin_name)
- [var plugin_type: es_sudo_plugin_type_t](/documentation/endpointsecurity/es_sudo_reject_info_t/plugin_type)
- [EndpointSecurity Enumerations](/documentation/endpointsecurity/endpointsecurity-enumerations)

### Enumerations

- [es_address_type_t](/documentation/endpointsecurity/es_address_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_address_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_address_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_address_type_t/rawvalue)
- [es_authentication_type_t](/documentation/endpointsecurity/es_authentication_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_authentication_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_authentication_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_authentication_type_t/rawvalue)
- [es_authorization_rule_class_t](/documentation/endpointsecurity/es_authorization_rule_class_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_authorization_rule_class_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_authorization_rule_class_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_authorization_rule_class_t/rawvalue)
- [es_auto_unlock_type_t](/documentation/endpointsecurity/es_auto_unlock_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_auto_unlock_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_auto_unlock_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_auto_unlock_type_t/rawvalue)
- [es_btm_item_type_t](/documentation/endpointsecurity/es_btm_item_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_btm_item_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_btm_item_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_btm_item_type_t/rawvalue)
- [es_gatekeeper_user_override_file_type_t](/documentation/endpointsecurity/es_gatekeeper_user_override_file_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_gatekeeper_user_override_file_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_gatekeeper_user_override_file_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_gatekeeper_user_override_file_type_t/rawvalue)
- [es_get_task_type_t](/documentation/endpointsecurity/es_get_task_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_get_task_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_get_task_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_get_task_type_t/rawvalue)
- [es_mount_disposition_t](/documentation/endpointsecurity/es_mount_disposition_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_mount_disposition_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_mount_disposition_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_mount_disposition_t/rawvalue)
- [es_mute_inversion_type_t](/documentation/endpointsecurity/es_mute_inversion_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_mute_inversion_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_mute_inversion_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_mute_inversion_type_t/rawvalue)
- [es_mute_inverted_return_t](/documentation/endpointsecurity/es_mute_inverted_return_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_mute_inverted_return_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_mute_inverted_return_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_mute_inverted_return_t/rawvalue)
- [es_od_account_type_t](/documentation/endpointsecurity/es_od_account_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_od_account_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_od_account_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_od_account_type_t/rawvalue)
- [es_od_member_type_t](/documentation/endpointsecurity/es_od_member_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_od_member_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_od_member_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_od_member_type_t/rawvalue)
- [es_od_record_type_t](/documentation/endpointsecurity/es_od_record_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_od_record_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_od_record_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_od_record_type_t/rawvalue)
- [es_openssh_login_result_type_t](/documentation/endpointsecurity/es_openssh_login_result_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_openssh_login_result_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_openssh_login_result_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_openssh_login_result_type_t/rawvalue)
- [es_profile_source_t](/documentation/endpointsecurity/es_profile_source_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_profile_source_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_profile_source_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_profile_source_t/rawvalue)
- [es_sudo_plugin_type_t](/documentation/endpointsecurity/es_sudo_plugin_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_sudo_plugin_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_sudo_plugin_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_sudo_plugin_type_t/rawvalue)
- [es_touchid_mode_t](/documentation/endpointsecurity/es_touchid_mode_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_touchid_mode_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_touchid_mode_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_touchid_mode_t/rawvalue)
- [es_xpc_domain_type_t](/documentation/endpointsecurity/es_xpc_domain_type_t)

#### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_xpc_domain_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_xpc_domain_type_t/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_xpc_domain_type_t/rawvalue)

## Structures

- [es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_t)

### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_cs_validation_category_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_cs_validation_category_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_cs_validation_category_t/rawvalue)
- [es_event_tcc_modify_t](/documentation/endpointsecurity/es_event_tcc_modify_t)

### Initializers

- [init()](/documentation/endpointsecurity/es_event_tcc_modify_t/init())
- [init(service: es_string_token_t, identity: es_string_token_t, identity_type: es_tcc_identity_type_t, update_type: es_tcc_event_type_t, instigator_token: audit_token_t, instigator: UnsafeMutablePointer<es_process_t>?, responsible_token: UnsafeMutablePointer<audit_token_t>?, responsible: UnsafeMutablePointer<es_process_t>?, right: es_tcc_authorization_right_t, reason: es_tcc_authorization_reason_t)](/documentation/endpointsecurity/es_event_tcc_modify_t/init(service:identity:identity_type:update_type:instigator_token:instigator:responsible_token:responsible:right:reason:))

### Instance Properties

- [var identity: es_string_token_t](/documentation/endpointsecurity/es_event_tcc_modify_t/identity)
- [var identity_type: es_tcc_identity_type_t](/documentation/endpointsecurity/es_event_tcc_modify_t/identity_type)
- [var instigator: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_tcc_modify_t/instigator)
- [var instigator_token: audit_token_t](/documentation/endpointsecurity/es_event_tcc_modify_t/instigator_token)
- [var reason: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_event_tcc_modify_t/reason)
- [var responsible: UnsafeMutablePointer<es_process_t>?](/documentation/endpointsecurity/es_event_tcc_modify_t/responsible)
- [var responsible_token: UnsafeMutablePointer<audit_token_t>?](/documentation/endpointsecurity/es_event_tcc_modify_t/responsible_token)
- [var right: es_tcc_authorization_right_t](/documentation/endpointsecurity/es_event_tcc_modify_t/right)
- [var service: es_string_token_t](/documentation/endpointsecurity/es_event_tcc_modify_t/service)
- [var update_type: es_tcc_event_type_t](/documentation/endpointsecurity/es_event_tcc_modify_t/update_type)
- [es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_t)

### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_tcc_authorization_reason_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_tcc_authorization_reason_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_tcc_authorization_reason_t/rawvalue)
- [es_tcc_authorization_right_t](/documentation/endpointsecurity/es_tcc_authorization_right_t)

### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_tcc_authorization_right_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_tcc_authorization_right_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_tcc_authorization_right_t/rawvalue)
- [es_tcc_event_type_t](/documentation/endpointsecurity/es_tcc_event_type_t)

### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_tcc_event_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_tcc_event_type_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_tcc_event_type_t/rawvalue)
- [es_tcc_identity_type_t](/documentation/endpointsecurity/es_tcc_identity_type_t)

### Initializers

- [init(UInt32)](/documentation/endpointsecurity/es_tcc_identity_type_t/init(_:))
- [init(rawValue: UInt32)](/documentation/endpointsecurity/es_tcc_identity_type_t/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/endpointsecurity/es_tcc_identity_type_t/rawvalue)

## Variables

- [var ES_CS_VALIDATION_CATEGORY_APP_STORE: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_app_store)
- [var ES_CS_VALIDATION_CATEGORY_DEVELOPER_ID: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_developer_id)
- [var ES_CS_VALIDATION_CATEGORY_DEVELOPMENT: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_development)
- [var ES_CS_VALIDATION_CATEGORY_ENTERPRISE: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_enterprise)
- [var ES_CS_VALIDATION_CATEGORY_INVALID: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_invalid)
- [var ES_CS_VALIDATION_CATEGORY_LOCAL_SIGNING: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_local_signing)
- [var ES_CS_VALIDATION_CATEGORY_NONE: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_none)
- [var ES_CS_VALIDATION_CATEGORY_OOPJIT: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_oopjit)
- [var ES_CS_VALIDATION_CATEGORY_PLATFORM: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_platform)
- [var ES_CS_VALIDATION_CATEGORY_ROSETTA: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_rosetta)
- [var ES_CS_VALIDATION_CATEGORY_TESTFLIGHT: es_cs_validation_category_t](/documentation/endpointsecurity/es_cs_validation_category_testflight)
- [var ES_EVENT_TYPE_NOTIFY_TCC_MODIFY: es_event_type_t](/documentation/endpointsecurity/es_event_type_notify_tcc_modify)
- [var ES_TCC_AUTHORIZATION_REASON_APP_TYPE_POLICY: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_app_type_policy)
- [var ES_TCC_AUTHORIZATION_REASON_ENTITLED: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_entitled)
- [var ES_TCC_AUTHORIZATION_REASON_ERROR: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_error)
- [var ES_TCC_AUTHORIZATION_REASON_MDM_POLICY: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_mdm_policy)
- [var ES_TCC_AUTHORIZATION_REASON_MISSING_USAGE_STRING: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_missing_usage_string)
- [var ES_TCC_AUTHORIZATION_REASON_NONE: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_none)
- [var ES_TCC_AUTHORIZATION_REASON_PREFLIGHT_UNKNOWN: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_preflight_unknown)
- [var ES_TCC_AUTHORIZATION_REASON_PROMPT_CANCEL: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_prompt_cancel)
- [var ES_TCC_AUTHORIZATION_REASON_PROMPT_TIMEOUT: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_prompt_timeout)
- [var ES_TCC_AUTHORIZATION_REASON_SERVICE_OVERRIDE_POLICY: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_service_override_policy)
- [var ES_TCC_AUTHORIZATION_REASON_SERVICE_POLICY: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_service_policy)
- [var ES_TCC_AUTHORIZATION_REASON_SYSTEM_SET: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_system_set)
- [var ES_TCC_AUTHORIZATION_REASON_USER_CONSENT: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_user_consent)
- [var ES_TCC_AUTHORIZATION_REASON_USER_SET: es_tcc_authorization_reason_t](/documentation/endpointsecurity/es_tcc_authorization_reason_user_set)
- [var ES_TCC_AUTHORIZATION_RIGHT_ADD_MODIFY_ADDED: es_tcc_authorization_right_t](/documentation/endpointsecurity/es_tcc_authorization_right_add_modify_added)
- [var ES_TCC_AUTHORIZATION_RIGHT_ALLOWED: es_tcc_authorization_right_t](/documentation/endpointsecurity/es_tcc_authorization_right_allowed)
- [var ES_TCC_AUTHORIZATION_RIGHT_DENIED: es_tcc_authorization_right_t](/documentation/endpointsecurity/es_tcc_authorization_right_denied)
- [var ES_TCC_AUTHORIZATION_RIGHT_LEARN_MORE: es_tcc_authorization_right_t](/documentation/endpointsecurity/es_tcc_authorization_right_learn_more)
- [var ES_TCC_AUTHORIZATION_RIGHT_LIMITED: es_tcc_authorization_right_t](/documentation/endpointsecurity/es_tcc_authorization_right_limited)
- [var ES_TCC_AUTHORIZATION_RIGHT_SESSION_PID: es_tcc_authorization_right_t](/documentation/endpointsecurity/es_tcc_authorization_right_session_pid)
- [var ES_TCC_AUTHORIZATION_RIGHT_UNKNOWN: es_tcc_authorization_right_t](/documentation/endpointsecurity/es_tcc_authorization_right_unknown)
- [var ES_TCC_EVENT_TYPE_CREATE: es_tcc_event_type_t](/documentation/endpointsecurity/es_tcc_event_type_create)
- [var ES_TCC_EVENT_TYPE_DELETE: es_tcc_event_type_t](/documentation/endpointsecurity/es_tcc_event_type_delete)
- [var ES_TCC_EVENT_TYPE_MODIFY: es_tcc_event_type_t](/documentation/endpointsecurity/es_tcc_event_type_modify)
- [var ES_TCC_EVENT_TYPE_UNKNOWN: es_tcc_event_type_t](/documentation/endpointsecurity/es_tcc_event_type_unknown)
- [var ES_TCC_IDENTITY_TYPE_BUNDLE_ID: es_tcc_identity_type_t](/documentation/endpointsecurity/es_tcc_identity_type_bundle_id)
- [var ES_TCC_IDENTITY_TYPE_EXECUTABLE_PATH: es_tcc_identity_type_t](/documentation/endpointsecurity/es_tcc_identity_type_executable_path)
- [var ES_TCC_IDENTITY_TYPE_FILE_PROVIDER_DOMAIN_ID: es_tcc_identity_type_t](/documentation/endpointsecurity/es_tcc_identity_type_file_provider_domain_id)
- [var ES_TCC_IDENTITY_TYPE_POLICY_ID: es_tcc_identity_type_t](/documentation/endpointsecurity/es_tcc_identity_type_policy_id)

## Type Aliases

- [es_statfs_t](/documentation/endpointsecurity/es_statfs_t)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
