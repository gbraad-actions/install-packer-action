Install Packer
==============

This simple GitHub Action installs Packer on the runner.


```yaml
- name: virtualization support
  uses: gbraad-actions/setup-virtualization@v2

- name: install packer
  uses: gbraad-actions/install-packer@v1
```

> [!NOTE]
> Ubuntu only. It is recommended to use the `setup-virtualization` action before installing Packer.
> And run `packer` after a session reload or using `sudo` to ensure the user is in the `qemu` group,
> otherwise Packer may not be able to use KVM and will run unaccelerated.
