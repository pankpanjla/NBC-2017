#!/bin/bash
# Note: This script is relay on password less ssh access for master_node
master_node_ip=10.10.10.126
master_node_user='root'
master_node_passwd='netweb'
passwd_file='/etc/passwd'
shadow_file='/etc/shadow'
group_file='/etc/group'
gshadow_file='/etc/gshadow'

tdir=`mktemp -d`
cd $tdir
pwd=`pwd`
if [ "$pwd" = "$tdir" ]
then
        echo "Successuflly created temp directory $tdir"
else
        echo "Unable to change to newly created temp dir $tdir"
        rm -rf $tdir
        exit 1
fi
for file in "$passwd_file" "$shadow_file" "$group_file" "$gshadow_file"
do
