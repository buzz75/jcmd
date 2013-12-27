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
