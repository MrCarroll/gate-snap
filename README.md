# Numerical simulations in medical imaging and radiotherapy, in a snap!
[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/gate)

## Intro
http://www.opengatecollaboration.org

Gate currently supports simulations of Emission Tomography (Positron Emission Tomography - PET and Single Photon Emission Computed Tomography - SPECT), Computed Tomography (CT), Optical Imaging (Bioluminescence and Fluorescence) and Radiotherapy experiments.
Using an easy-to-learn macro mechanism to configurate simple or highly sophisticated experimental settings, GATE now plays a key role in the design of new medical imaging devices, in the optimization of acquisition protocols and in the development and assessment of image reconstruction algorithms and correction techniques.
It can also be used for dose calculation in radiation therapy, brachytherapy or any other application.

This snap contains Gate bundled with Geant4 (with QT, and all optional Geant4 datasets), ROOT, and PyTorch.
Simply run `Gate` or `Gate --qt` on the command line to begin using it.

Snaps are sandboxed applications designed to be portable and run across a wide variety of Linux systems.
Due to the sandboxing, please ensure all your work is contained within your `$HOME` folder to be accessible.

Please consider installing the `root-framework` snap in order to make `root` and other binaries also available on your system.
This is not required to use the Gate snap, but may be desired by people who wish to use ROOT to analyse their output.
Simply run `sudo snap install root-framework` or visit https://snapcraft.io/root-framework for more information.

This product includes software developed by Members of the Geant4 Collaboration ( http://cern.ch/geant4 )

## Building

This repository can be built by simply invoking the `snapcraft` utility.
Snapcraft is the build system for snaps and can be installed itself as a snap [here](https://snapcraft.io/snapcraft).
A basic guide to using Snapcraft can be found [here](https://snapcraft.io/docs/snapcraft-overview).
If the user does not have a system compatible with Multipass, I.E, due to lack of virtual machine CPU support, consider using the LXD backend, instructions available [here](https://snapcraft.io/docs/build-on-lxd). 

In essence, building the gate snap involves setting up snapcraft, cloning this repository and simply running:
```bash
snapcraft
sudo snap install Gate.snap --dangerous
sudo snap alias gate Gate
```

## Support
Presently, this package is a solo endevour done on a best effort basis.
If this package isn't working for you, consider using the [Gate Docker package](https://opengate.readthedocs.io/en/latest/docker_gate.html) or the [VGate virtual machine image](https://opengate.readthedocs.io/en/latest/vgate.html).

I am welcome to feedback about any issues however.

## Licensing
Please note that whilst this repository is under MIT licensing, the components distributed within have various licenses.

This product includes software developed by Members of the Geant4 Collaboration ( http://cern.ch/geant4 )

Geant4 source may be found at https://geant4.web.cern.ch/support/download

ROOT is LGPL 2.1, its license may be found [here](https://github.com/root-project/root/blob/master/LICENSE) and its source may be found [here](https://github.com/root-project/root.git).

PyTorch has a BSD style license that may be viewed [here](https://github.com/pytorch/pytorch/blob/master/LICENSE) and its source code viewed [here](https://github.com/pytorch/pytorch).

The Insight Toolkit (ITK) is licensed under the Apache 2.0 license, its license may be viewed [here](https://github.com/InsightSoftwareConsortium/ITK/blob/master/LICENSE) and its source [here](https://github.com/InsightSoftwareConsortium/ITK/blob/master/LICENSE)

Documentation of the included Ubuntu packages in the snap can be found in `/snap/root-framework/current/usr/share/doc` and accessed at [https://packages.ubuntu.com/](https://packages.ubuntu.com/).
