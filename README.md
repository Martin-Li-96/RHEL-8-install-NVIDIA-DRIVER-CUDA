RHEL-8-install-NVIDIA-DRIVER-CUDA
INSTALL NVIDIA-DRIVER
#sudo systemctl set-default multi-user.taget
#reboot
s#udo sh ./NVIDIA-Linux-x86_64-515.57.run

At first time to run nvidia installer, it will write file to disable the nouveau module, and then run "dracut --force" command 
and tehn reboot

sudo yum install kernel-debug-devel dkms -y # to use dkms
Run NVIDIA-Linux-x86_64-515.57.run again, it will finished the installation 
sudo systemctl set-default graphical.target


#sudo sh ./cuda_11.7.0_515.43.04_linux.run
and then add cuda to path

#sudo cat <<EOF >> /etc/profile
#export PATH=/usr/local/cuda-11.7/bin${PATH:+:${PATH}}
#export LD_LIBRARY_PATH=/usr/local/cuda-11.7/lib64\${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
#EOF

