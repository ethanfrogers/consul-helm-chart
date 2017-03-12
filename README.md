# Consul Helm Chart

This is a Helm Chart for Hashicorp Consul based on Kelsey Hightower's [`consul-on-kubernetes`](https://github.com/kelseyhightower/consul-on-kubernetes) tutorial. _This is in no way meant for production use!_

This chart will install a 3 node Consul cluster using a Kubernetes StatefulSet. Once all of the nodes have been provisioned, a job will run that will join all the nodes to the leader.

One downfall is that this chart relies on a Secret already existing with `ca.pem`, `consul-key.pem`, & `consul.pem`. To see how to do that, check out Kelsey's repo.

## Motivation

I wanted to give writing my own Helm Chart a shot. I thought a Consul cluster would be an easyish start. 


## Required Configuration

- `gossipSecret` - Suggested `consul keygen`
- `secretName` - Kubernetes secret containing `ca.pem`, `consul-key.pem`, `consul.pem`

## Future

- [ ] Auto provision certs for node to node communication



