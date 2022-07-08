# PlantUML AWS Color Palette

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

!define usersSprite img:https://raw.githubusercontent.com/coregen/plantuml-aws-color-palette/master/examples/unicorn-sprite.png{scale=0.8}
!define gitSprite img:https://raw.githubusercontent.com/plantuml-stdlib/gilbarbara-plantuml-sprites/master/pngs/git.png{scale=1.2}

!$legacy_bg = AWSColor("bg3", "light")
!$legacy_border = AWSColor("orange", "light")
!$legacy_font = AWSColor("fg1", "light")
!$actor_background = AWSColor("turquoise", "dark")
!$actor_border = AWSColor("purple", "dark")
!$actor_font = AWSColor("fg1", "dark")

AddPersonTag(unicorns, $bgColor=$actor_bg, $borderColor=$actor_border, $fontColot=$actor_font, $legendText="Unicorn Workload")
AddContainerTag(legacy, $bgColor=$legacy_background, $borderColor=$legacy_border, $legacy_font, $legendText="Unicorn Workload")

Person(webapp, "Unicorn Squad", "Equus Unicorae", "Git and CI/CD experts, using purple horn magic to maintain legacy code", $tags="unicorns")
Container(legacy_code, "Legacy Code Noodles", "Yakisoba", "Legacy code in the form of deep fried soba noodles", $tags="legacy")

LAYOUT_WITH_LEGEND()
SHOW_LEGEND()

@enduml
```

![example](https://raw.githubusercontent.com/andecy64/plantuml-aws-color-palette/master/examples/unicorns.svg)

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
