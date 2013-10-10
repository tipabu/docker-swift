docker-swift
============

Docker image for Swift all-in-one demo deployment

This is an attempt to dockerize the instructions for a [Swift All-in-one deployment](http://docs.openstack.org/developer/swift/development_saio.html). 

It is not yet complete.

##Notes on changes

- user and group ids are swift:swift
- the instructions provide for using a separate partition or a loopback for storage, presumably to allow the storage capacity to be strictly limted. Neither of these was easy for a Docker n00b to implement, so I've just used /swift, with symbolic links in /srv. The storage can be limited at the OS level in the Docker image if it's a concern.
- the Github sources are cloned to /usr/local/src
