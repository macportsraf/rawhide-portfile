# README

My version of my rawhide macports Portfile.

It differs from the official Portfile only slightly:

 - It includes all four download sites, rather than just one

# INSTALL

You can either install using the official macports Portfile:

    sudo port install rawhide

Or via this Portfile (but there's no reason to):

    cd ~/src
	git clone https://github.com/macportsraf/rawhide-portfile
	mkdir ~/ports
	cp -pr rawhide-portfile/sysutils ~/ports
	rm -rf rawhide-portfile
	cd ~/ports
	portindex
	echo file://$(pwd) >> /opt/local/etc/macports/sources.conf
	# Edit the file to put the `file` URL above the main `rsync` URL
	vim /opt/local/etc/macports/sources.conf

