#JCMD

##Introduction:  

go: Easy change your directory  
flash: Easy flash your device  
install: Easy install your file  

##How to Use:  

###1. Add below to your .bashrc:
<pre><code>if [ -n "$BASH_VERSION" ]; then  
    # include .bash_completion if it exists  
    if [ -f "$HOME/jcmd/.bash_completion" ]; then  
        . "$HOME/jcmd/.bash_completion"  
    fi  
fi  

export  PATH=$HOME/jcmd:$PATH  
</code></pre>

###2. Put files in your linux  
<pre><code>$ cd ~  
$ git clone https://github.com/buzz75/jcmd.git  
$ source ~/.bashrc  
</code></pre>

###3. Edit your mycmd config file
#### 3.1 Go to your project home, you can use *`go`* 
<pre><code>$ emacs ~/.mycmd_conf  
</code></pre>
<pre><code>[core]  
project_home = /home/username/project/  <---- 
</code></pre>

#### 3.2 Go to your project home, you can use *`go project`* 
your a9 project at /home/username/project/a9, you can use `ezg a9` 

<pre><code>[project]  
a9 = ics-robin
pm = ics-mr1.1-pm  
log = ../test_log/
</code></pre>


#### 3.3 Setting your sub-directory  *`go project subdir`* 
Using "go project sub-directory" to sub-directory  
ex. $ go pm i2c  
<pre><code>[subdir]  
i2c = kernel/drivers/i2c  
uart = kernel/drivers/tty/serial  
eeprom = kernel/drivers/misc/eeprom  
</code></pre>

#### 3.4 Setting your sub-directory for different project 
Create section [xxx_dir]  
Using `ezg project sub-directory` to sub-directory  
ex. $ `ezg project xxx`  
You also can set default option, if you have many project with same directory 
<pre><code>[out_dir]  
prefix = out/target/product  
a9 = a9  
pm = picasso_m  
pmf = picasso_mf  
pre-jb-pmf = picasso_mf  
pe = picasso_e  
pe2 = picasso_e2  
p1 = picasso  
vg = vangogh  
</code></pre>
you can use `ezg a9 mach`, change directory to /home/username/project/a9/kernel/arch/arm/mach-msm 
<pre><code>[mach_dir]   
prefix = kernel/arch/arm  
default = mach-tegra  
a9 = mach-msm  
</code></pre>

