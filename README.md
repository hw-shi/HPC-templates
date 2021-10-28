# HPC-templates

This is a dropbox sharing HPC scripts for [Quntao Zhuang's quantum information theory group](https://sites.google.com/view/quntaozhuang).

## SLURM test
Run a job array with customized argument input on the HPC based on SLURM.

1. Upload the bash script "SLURMtest" to directory "scripts/test" and the wolfgram script SLURMtest.wl to directory "test";
2. Submit the bash script "SLURMtest". For example, to submit a 5-job array with argument m=1,2,3 respectively, use the following code:
```
   for mm in {1..3}; do sbatch -a 1-5 --export m=$mm scripts/test/SLURMtest ;done
```
