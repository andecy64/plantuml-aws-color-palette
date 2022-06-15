# PlantUML AWS Colors

The purpose of this project is to provide
a set of PlantUML variables containing
colors usually seen in AWS documentation
and websites.  

In addition, a procedure that creates
samples to display those colors is available
for convenience.  

The HEX codes for the colors were taken from
[this][aws-color-palette-article] article written
by Adrian Simionov.

## How to use

Example using C4-PlantUML

```plantuml
@startuml

!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml
!include https://raw.githubusercontent.com/coregen/plantuml-aws-color-palette/master/dist/aws-colors.puml

!$unicorns_bg = AWSColor("bg2", "dark")
!$unicorns_border = AWSColor("orange", "dark")

AddContainerTag(unicorns, $bgColor=$unicorns_bg, $borderColor=$unicorns_border, $legendText="Unicorn Workload")

Container(webapp, "Web Application", "Python", "Gives out Unicorns", $tags="unicorns")

LAYOUT_WITH_LEGEND()
SHOW_LEGEND()

@enduml
```

![example](example/unicorns.svg)

## Available Colors

There are two schemes

* dark
* light

For each scheme, the following colors are available

* bg1
* bg2
* bg3
* bg4
* fg1
* fg2
* orange
* red
* pink
* purple
* blue
* cyan
* turquoise
* green

[aws-color-palette-article]: https://adrian.simionov.io/aws/2020/04/24/aws-color-palette.html
!function AWSColor($colorname, $scheme)
