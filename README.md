# docker-elasticsearch
simple docker file for elastic search 

## run

```bash
$ docker build -t myelasticsearch-data elasticsearch-data/.
$ docker build -t myelasticsearch-master elasticsearch-master/.
$ docker run -d -p 9200:9200 --volumes-from=elasticsearch-data --name=elasticsearch-master myelasticsearch-master
```

## Note

If you see error message about virtual memory size, you have to increase your virtual memory size by `sudo sysctl -w vm.max_map_count=262144`.

The virtual memory changes will be lost after reboot. To change it permanently, you have to modify the /etc/sysctl.conf file.
