# Fedora 32

## Update everything

```bash
sudo dnf upgrade
```

## Install programs

### Chrome

```bash
sudo dnf install https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm
```

### VS code

Taken from https://code.visualstudio.com/docs/setup/linux#_rhel-fedora-and-centos-based-distributions

```bash
# step 1, import the package signing GPG key
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
# step 2, add content to a new file /etc/yum.repos.d/vscode.repo
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
# step 3, install vscode
sudo dnf install code
```

If you get an error message like this (and more) in the first step:

```
error: db5 error(-30969) from dbenv->open: BDB0091 DB_VERSION_MISMATCH: Database environment version mismatch
```

Try this (taken from https://bugzilla.redhat.com/show_bug.cgi?id=1461392#c8):
```bash
sudo dnf clean dbcache
```

### R and Rstudio

```bash
sudo dnf install R
sudo dnf install rstudio-desktop
```

### Docker

Use `podman`. It is probably pre-installed (if not: `sudo dnf podman`).

If you want to use the `docker` command you can add the following line to your `.bashrc` file (or equivalent):

```bash
alias docker=podman
```
