
- To boot use USB 2.0 media or burn a DVD

- To discard old Boot Environments and free storage:

`beadm list | grep openindiana-2024:0[1-4] | awk '{ print $1 }' | tac | while read i ; do sudo beadm destroy -vsF $i ; done`
