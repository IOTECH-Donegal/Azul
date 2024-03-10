# Introduction

I started this project in 2021.

Despite all the really good videos and notes on the Internet, I have yet to find a single, idiot's guide to building an **Autonomous Surface Vehicle (ASV)** or an **Autonomous Underwater Vehicle (AUV)**. This repo contains all notes and code for the Arduboat based ASV, the first step to an AUV.

The primary purpose for this vessel is for taking video/photographs for photogrammetry. The specification is for:

* RTK positioning accuracy of c. 1cm
* Heading response at 5Hz with 0.5° These values will need to be available as meta data for video/camera.

A second option is to use an INS to maintain positional accuracy under piers or in caves.

This platform can support an Airmar SS510 for hydographic survey and a transom mount transducer for seabed search.

Apart from being a central repo, this material is mostly public domain, please treat it as licensed to Creative Commons (CC BY 4.0). If you copy or share the information, you must attribute it to its source (here!). Any subsystem complete for alpha test will be marked so. Anything else will be marked as **Work-in-Progress (WIP)** or **Not Started**.

A bill of material (BOM) will only be completed when an alpha vessel first sets sail.

* Length: 1850mm
* Width: 610 mm
* Height: 230mm
* Weight: 8.1kg

Using latest versions of code from [here](https://github.com/rtklibexplorer/RTKLIB/releases).
