## ViVe

ViVe is a C# library you can use to make your own programs that interact with the A/B feature experiment mechanism found in Windows 10 & newer.

The *FeatureManager* class should cover most feature management needs with the added benefit of some struct heavy lifting being done for you. Boot persistence and LKG management is offered exclusively by this class as it had to be reimplemented.

In case you'd like to talk to NTDLL exports directly, you can use *NativeMethods*.

## ViVeTool

ViVeTool is both an example of how to use ViVe, as well as a straightforward tool for power users which want to use the new APIs instantly.

[![Release downloads](_resources/68747470733a2f2f696d672e73686965_bea160bf09064dabb.svg)](https://github.com/thebookisclosed/ViVe/releases/)

## Compatibility

In order to use ViVe, you must be running Windows 10 build 18963 or newer.

![](_resources/68747470733a2f2f692e696d6775722e_673e7a90b3464c8fb.png)