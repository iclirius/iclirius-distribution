## v1.0.0-rc.33

Bonjour registration contract fix. The secure publisher now passes `_iclirius._tcp` as the native registration type and `local.` as its domain, matching macOS `dns-sd -R`. Startup diagnostics capture bounded native output when registration fails. Physical CLUSTER-3 acceptance remains pending.

Source revision: `64abcd44d90c7dd956ed237955947956eade4cc6`

Artifact: `iclirius-1.0.0-rc.33.tar.gz`
SHA-256: `7badff79b2d224b9732533fe3e43a6f6a6c6e69bd92a4ce1ba5c72d320abd96f`

Wheel: `iclirius_openclaw-1.0.0rc33-py3-none-any.whl`
SHA-256: `889b23744583e72a8854d3caeb81f84f56d0e40523f438b73f16d3a790fc82da`

## v1.0.0-rc.32

Secure discovery readiness candidate. A live TLS listener with a failed Bonjour publisher is now reported as DEGRADED with a bounded failure reason, and Doctor/repair expose the issue. Runtime state roots are propagated consistently. Physical CLUSTER-3 acceptance remains pending.

Source revision: `3cee4c0ef05143b317c3449b2217190fd980e1de`

Artifact: `iclirius-1.0.0-rc.32.tar.gz`
SHA-256: `f63fbe86293f0e280981ab36da0be01ef7206bc4eef3d06c1948e8075112aedc`

Wheel: `iclirius_openclaw-1.0.0rc32-py3-none-any.whl`
SHA-256: `8d2d8f0f83fb3f522811adb75ab6c2ca9ac8d914c1a91dc94b3492b3ba6bc137`

## v1.0.0-rc.31

Managed secure Bonjour lifecycle. RC30 physical validation found that the TLS listener could be live while launchd failed to publish `_iclirius._tcp.local.` because `dns-sd` was resolved only through the shell PATH. RC31 resolves the system tool explicitly, owns publisher lifecycle with the secure listener, and adds bounded mobility diagnostics. Physical CLUSTER-3 acceptance remains pending.

Source revision: `9768123033f4ca84a4e79597482cfe8334ce422f`

Artifact: `iclirius-1.0.0-rc.31.tar.gz`
SHA-256: `82532cf184f846474e05c5fa97ac191276a38d781a9de046cd10f80290272ea8`

Wheel: `iclirius_openclaw-1.0.0rc31-py3-none-any.whl`
SHA-256: `40b3fbdb92539033ec002cbb191c3326beb0074a764cdc661ddc23fc1b0cb74f`

## v1.0.0-rc.30

CLI discovery dispatch fix. RC29's endpoint-mobility import shadowed the
module-level `discover` binding and caused `node discover --json` to fail before
discovery ran. RC30 fixes the production dispatch path while preserving
authenticated trusted endpoint mobility.

Source revision: `f802542b68b472a85204f0bd3dc54e938a50c1b0`

Artifact: `iclirius-1.0.0-rc.30.tar.gz`
SHA-256: `97c949009e77a78fdb3e5ca5ef8c929211d1ab8657d64b618ab608fca16e073f`

## v1.0.0-rc.29

Trusted endpoint mobility candidate. A stale address for an already trusted
peer is refreshed only after bounded Bonjour discovery and an authenticated
TLS 1.3 PING/PONG using the pinned Ed25519 identity. The managed secure
listener advertises its actual 18891 endpoint; enrollment remains separate.

Source revision: `57a5b230c3edd2fe0e588eb89f40f71a841e90c5`

Artifact: `iclirius-1.0.0-rc.29.tar.gz`
SHA-256: `00c83a9ddfc88f629f7de4469c42ac741b74051aeb5c76b790e95f1badb2e877`

## v1.0.0-rc.2

Release candidate with Doctor deep diagnostics, NodeCapabilityProfile, role-aware node repair/bootstrap, Ed25519 node identity, TLS node transport, explicit pairing, and authenticated ping/pong. Remote execution, heartbeat, capability exchange, and real two-Mac acceptance remain future work.

Artifact: `iclirius-1.0.0-rc.2.tar.gz`
SHA-256: `5422e2d7f4c78ac496cd21870cab87e72df50237a61634cec7aca47d4c4251e`
