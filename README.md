# hssllvmsetup

**Strong Suggestion: Use a Docker container.**

Setup scripts to install and configure LLVM

This is a basic starter repo designed for writing LLVM passes to help Holistic Software Security Course.

## Installing LLVM

```
wget https://apt.llvm.org/llvm.sh
chmod +x llvm.sh
sudo ./llvm.sh <version number>
sudo ln -s /usr/bin/clang-12 /usr/bin/clang
sudo ln -s /usr/bin/clang++-12 /usr/bin/clang++
sudo ln -s /usr/bin/llvm-config-12 /usr/bin/llvm-config
sudo ln -s /usr/bin/opt-12 /usr/bin/opt
```
We will be using LLVM 12 in our course. So, you should be installing version 12, i.e., `sudo ./llvm.sh 12`

## Installing Z3

```
wget https://github.com/Z3Prover/z3/releases/download/z3-4.8.11/z3-4.8.11-x64-glibc-2.31.zip
unzip z3-4.8.11-x64-glibc-2.31.zip
cd z3-4.8.11-x64-glibc-2.31
pwd
```
Export the path where you extracted the above z3 zip file (i.e., path given by `pwd`).

Add the following line at the end of your `~/.bashrc`
```
export Z3_DIR=<extracted z3 zip>
```

Refer [llvm-passes](https://github.com/purs3lab/hssllvmsetup/tree/main/llvm-passes) folder for sample passes.
