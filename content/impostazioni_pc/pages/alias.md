---
title: Alias
type: docs
weight: 2
---

>
alias containers='dockerps && podmanps'  
alias containersa='dockerpsa && podmanpsa'  
alias dockerps='docker ps --format '\''table {{.ID}}\t{{.Image}}\t{{.Status}}\t{{.Names}}'\'''  
alias dockerpsa='docker ps -a --format '\''table {{.ID}}\t{{.Image}}\t{{.Status}}\t{{.Names}}'\'''  
alias douroot='sudo chmod -R 777 /home/plraska/Desktop/Attilio/Gatcha/doujinshi/'  
alias hdd='sudo mount -t ntfs-3g -o remove_hiberfile /dev/sda1 /media/plraska/'  
alias l='ls -ltrh'  
alias la='ls -Ah'  
alias ll='ls -lh'  
alias log-out='gnome-session-quit'  
alias ls='ls --color=auto'  
alias myip='ifconfig wlo1 | grep '\''inet '\'' | awk '\''{print $2}'\'''  
alias nhentai='docker run --rm -it -v /home/plraska/Desktop/Attilio/Gatcha/doujinshi:/output -v ~/.nhentai/:/root/.nhentai nhentai'  
alias podmanps='podman ps --format '\''table {{.ID}}\t{{.Image}}\t{{.Status}}\t{{.Names}}'\'''  
alias podmanpsa='podman ps -a --format '\''table {{.ID}}\t{{.Image}}\t{{.Status}}\t{{.Names}}'\'''  
alias puntata='py /home/plraska/Desktop/Programmazione/varie/script_uni/puntata_telefilm.py'  
alias py='python3.12'  
alias qBittorrent='docker start qbittorrent'  
alias raspberry='ssh pi4@192.168.1.61'  
alias sort='du -hs * | sort -h'  
alias update='sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get dist-upgrade -y'  
alias youtube='ytfzf'  
>

>
nhfunction() {  
nhentai --id "$1"  
douroot  
cd /home/plraska/Desktop/Attilio/Gatcha/doujinshi  
py convert_2_pdf.py  
}

wiki(){  
cd /home/plraska/hugo/mywiki  
hugo server  
}

>