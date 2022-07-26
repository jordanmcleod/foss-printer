# foss-printer

Physical printers are still necessary sometimes but we do not yet have a FOSS-aligned alternative.  This project seeks to design, source, and build a physical printer with FOSS fundamentals that use purpose-built FOSS that should be adaptable to any OS so that anyone can build a printer with fully transparent operations with re-usable (and re-fillable) ink cartridges to reduce e-waste.

The intial phases of this project will be to design a printer using parts that can readily be obtained using a variety of controllers to allow anyone, worldwide to build a printer from modular components.  Using modular components should also benefit the reduction of e-waste by allowing the components of the printer to be re-used in other projects if the printer is no longer required (or is made sufficiently obsolete by the community maintaining this project).

Presently, this project will be split into the following paths:

## foss-printer/docs
- /hardware
- /print-mediums
- /software
- /templates
  - design requirements documentation (to be created)
  - design implementation documentation (to be created)
  - implementation test plan documentation (to be created)

## foss-printer/hardware
- hardware design and schematics
- research of components
  - controllers
  - print system
    - jet (ink)
    - laser (powder)
    - phaser (wax) 
    - thermal (paper)

## foss-printer/print-media
- research of print media
  - liquid ink
    - cartridge
    - print heads
    - pigment colors
    - viscosity
  - powdered ink
    - cartridge
    - particle sizes
    - pigment colors
    - print heads
  - thermal
    - "paper"
    - print heads
    - temperature
  - wax blocks
    - composition
    - print heads
    - sizes

## foss-printer/software
- drivers
- GUI

## foss-printer/tests
- unittests
- workflow tests


# Standards

This project seeks to be easily accessible, even to novice contributors.  As such, all design decisions for hardware and software need to be documented using the design documention templates, which will ease the eventual burden of writing and maintaining a comprehensive manual (or wiki) for building and operation of the desired product.

Python 3 is the preferred language.  Additionally, unittests of individual methods and workflow testing of multiple classes is desired via pytest to encourage CI/CD.  Although each method requires an initial unittest, it will likely be more beneficial for test cases to be written or enhanced by contributors that are not the author of the original method so that less bias is introduced when testing methods and workflows.

It may be easiest to begin with a standard, well-documented platform, such as a Raspberry Pi, to act as a controller for a printer.  A Raspberry Pi would allow, depending on its model, connectivity over multiple sources.

Presently, without discussion, it is yet undetermined for which media the printer will support initially.  Optimally, in the future, slight build modifications will allow any of the four (liquid ink, powdered ink, thermal, wax) types of printer media to be used when building this printer.


- Summary:
  - Documentation: 
    - design requirements documentation
    - design implementation documentation
    - implementation test plan documentation
  - Hardware:
    - standard platform; e.g., Rasperry Pi
      - allows, depending on model, multiple connectivity sources: BT, Ethernet, USB, WiFi
    - FOSS modling projects are highly encouraged for schematics
      - [FreeCAD](https://www.freecadweb.org/downloads.php)
      - [SolveSpace](https://solvespace.com/download.pl)
    - Tests
  - Print Media:
    - liquid ink (jet)
    - powdered ink (laser)
    - thermal ("receipt" paper)
    - wax (phaser)
  - Software:
    - Languages: 
      - Python 3.10+
        - Linter: TBD
        - Formatter: TBD
      - MySQL
    - Tests:
      - each test name is preceeded by "test_"
      - Each method requires a unittest
      - Each workflow requires a test


# Disclaimer

I have created this project in a public space so that, hopefully, a community will develop around it.  I do not have enough specialized knowledge to undertake this on my own.  I have had this idea for a long time as well as some other projects, which should have FOSS-aligned, maintained alternatives, that do not yet exist.
