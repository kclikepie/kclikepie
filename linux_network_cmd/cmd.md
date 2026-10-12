## CMD list

### Status check
```sh
ethtool enp2s0f0
ethtool -i enp2s0f0
ethtool -S enp2s0f0
ip neigh show
ip -s link show enp2s0f0
ip -d link show enp2s0f0
dmesg -T|tail -50
cat /proc/softirqs
ifconfig
```

### Stress

```sh
iperf3 -R -P 4
```

### Surveillance

```sh
watch -n $SEC $target_cmd
```

### Set

```sh
sudo ip link set enp2s0f0 down
sudo ip link set enp2s0f0 up
```

