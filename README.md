# Docker Swarm Cheatsheet

## Nodes Management
- List docker nodes : docker node ls
- Drain a node : docker node update --availability drain <node_name>
- UNDO Drain a node : docker node update --availability active <node_name>
- Add label to node :   docker node --label-add <key>=<value> <node_name>
- Remove label from node :   docker node --label-rm <key> <node_name>
- Lookup node label   docker node inspect <node_name> | grep Labels -C5


## Services Management
- List services on manager: docker service ls
- Describe services on manager: docker service ps <service_name>
- Inspect service : docker service inspect <service_name>
- Scale service : docker service scale <service_name>=<replicas>
- Remove service : docker service rm <service_name>

## Stack Management
- List stacks: docker stack ls
- Remove stack : docker stack rm <stack_name>
