irule-99bottles
===============

99 Bottles of Beer in iRules.

# Add iRule irule.99bottles to your BIG-IP
# Create virtual service with iRule associated
# ???
# profit

```
  tmsh create / ltm virtual vip.99bottles.10000 { \
     destination x.x.x.x:10000 ip-protocol tcp \
     mask 255.255.255.255 rules { irule.99bottles } \
     profiles add { tcp {} http {} } }

```

cURL to see the result.

```
  curl -x '' -s0 http://x.x.x.x:10000/
```

.
