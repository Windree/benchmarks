# benchmarks

## zstd compression level benchmark
```bash
for i in `seq 1 19`; do echo $i; dd if=/dev/sda bs=1G count=1 2> 1G-`printf %02d $i`.zstd.txt | zstd -$i > 1G-`printf %02d $i`.zstd ; done
```
## lzo compression level benchmark
```bash
for i in `seq 1 9`; do echo $i; dd if=/dev/sda bs=1G count=1 2> 1G-`printf %02d $i`.lzo.txt | lzop -$i > 1G-`printf %02d $i`.lzo ; done
```
