__IMPORTANT NOTE__: It it no longer possible to build the documentation due to various changes over time in the yum repository, Docker, and pgBackRest. The [backup-training.html](https://github.com/pgbackrest/training/blob/master/backup-training.html) file in this repo is the output of a prior, successful build.

---

# Practical PostgreSQL Backup & Restore

Practical PostgreSQL backup & restore using the core tools and pgBackRest.

# Download required tools

1) Download and install VirtualBox:

https://www.virtualbox.org/wiki/Downloads

2) Download and install Vagrant:

https://www.vagrantup.com/downloads.html

# Build the VM

1) Clone the training repository into a local directory using git:
```
git clone https://github.com/pgbackrest/training.git
```

Or download from https://github.com/pgbackrest/training as a ZIP file.  Click on "Clone or download" to get the ZIP download button.

2) Build the Vagrant VM:
```
cd training (or training-master if ZIP downloaded)
vagrant up
```

# Build the Documentation

1) Logon to the Vagrant VM:
```
vagrant ssh
```

2) Build the documentation:
```
/docdynamo/doc/doc.pl --no-cache --doc-path=/training/doc
```

3) Check that `training/backup-training.html` was created.
