# Vault

## Unseal

```bash
oc exec -ti vault-0 -- vault operator init
oc exec -ti vault-0 -- vault operator unseal
oc exec -ti vault-0 -- vault operator unseal
oc exec -ti vault-0 -- vault operator unseal

oc exec -ti vault-1 -- vault operator raft join http://vault-0.vault-internal:8200
oc exec -ti vault-1 -- vault operator unseal
oc exec -ti vault-1 -- vault operator unseal
oc exec -ti vault-1 -- vault operator unseal

oc exec -ti vault-2 -- vault operator raft join http://vault-0.vault-internal:8200
oc exec -ti vault-2 -- vault operator unseal
oc exec -ti vault-2 -- vault operator unseal
oc exec -ti vault-2 -- vault operator unseal
