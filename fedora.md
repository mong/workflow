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

```bash
# step 1
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
# step 2
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
# step 3
sudo dnf install code
```

If you get an error message like this (and more) in the first step:

```
error: db5 error(-30969) from dbenv->open: BDB0091 DB_VERSION_MISMATCH: Database environment version mismatch
```

Try this:
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
