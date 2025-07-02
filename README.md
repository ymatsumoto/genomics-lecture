# Short instruction for lecuture
## Gitpod
Access to [gitpod website](https://www.gitpod.io/gitpod-or-classic) and activate a container from gitpod via https://github.com/ymatsumoto/tmp

## Get files for demo
https://tinyurl.com/k59en9pp


## Command list
```bash
gitpod:~$ unicycler -1 short_reads_1.fastq.gz -2 short_reads_2.fastq.gz -t 4 -o assembly_short
gitpod:~$ cp short_reads_1.fastq.gz check.fastq.gz
gitpod:~$ gunzip check.fastq.gz
```

```bash
gitpod:~$ Bandage image assembly_short/assembly.gfa assembly_short/assembly.png
```

```bash
gitpod:~$ seqkit stat assembly_short/assembly.fasta
```

```bash
gitpod:~$ nucmer reference.fasta assembly_short/assembly.fasta --delta short.delta
gitpod:~$ mummerplot --png -R reference.fasta -Q assembly_short/assembly.fasta --layout short.delta -p short
```

```bash
gitpod:~$ dfast -g assembly_short/assembly.fasta -o assembly_short/dfast
```
