# SM7675 GPU platform operations

The ShengGmu and ShengGpuSmmu interfaces are imported from UniXNU-sm8550-common
main a9f45dc60c035084b95463781538380f4c3606c9. Runtime symbols and source names
are preserved. Generated uke headers supply gen7_11_0 windows, firmware and votes.
Board votes and firmware selection remain in the device repository.

The OEM DT declares one nonsecure user route, SID 0. The sheng-only second
route is not leased on uke; secure SID 2 is not attached to an ordinary process VM. GMU uses SID 5. The OEM GPU ACTLR policy is 0x32b.
These are source inputs; the iPadOS 27 integration awaits device qualification.
