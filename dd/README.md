# dd
#Write performance
dd if=/dev/zero of=tempfile bs=1M count=1024
#Clear read cache
sudo sysctl -w vm.drop_caches=3
#Read performance
dd if=tempfile of=/dev/null bs=1M count=1024