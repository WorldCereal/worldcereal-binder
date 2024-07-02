[![Binder](https://replay.notebooks.egi.eu/badge_logo.svg)](https://replay.notebooks.egi.eu/v2/gh/WorldCereal/worldcereal-binder/HEAD)
# WorldCereal Binder Environment 
This helper repository contains the configuration required to setup a Binder environment that can run the WorldCereal system.

To update:

### 1. Update `worldcereal.yml` with required packages

Add specific version of required packages.

### 2. Create a new `lock` file

conda-lock -k explicit -f worldcereal.yml -p linux-64

### 3. Optionally install and test the new environment using `mamba`

```
mamba create -y -n python310 --file conda-linux-64.lock
```

### 4. Push to the repository and launch binder

This way the new docker image will be built (which can take some time).

[![Binder](https://replay.notebooks.egi.eu/badge_logo.svg)](https://replay.notebooks.egi.eu/v2/gh/WorldCereal/worldcereal-binder/main)

