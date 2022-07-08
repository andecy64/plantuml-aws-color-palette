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

!define unicornSprite img:https://publicdomainvectors.org/photos/Unicorn-Silhouette-7.png{scale=0.3}
!define gitSprite img:https://raw.githubusercontent.com/plantuml-stdlib/gilbarbara-plantuml-sprites/master/pngs/git.png{scale=1.2}

!$legacy_bg = AWSColor("bg3", "light")
!$legacy_border = AWSColor("orange", "light")
!$legacy_font = AWSColor("fg1", "light")
!$actor_bg = AWSColor("purple", "dark")
!$actor_border = AWSColor("turquoise", "dark")
!$actor_font = AWSColor("fg2", "dark")

!$fixer_color = AWSColor("fg1", "light")

AddPersonTag(unicorns, $bgColor=$actor_bg, $borderColor=$actor_border, $fontColor=$actor_font, $legendText="Expert Equus")
AddContainerTag(legacy, $bgColor=$legacy_bg, $borderColor=$legacy_border, $fontColor=$legacy_font, $legendText="Internal Infrastructure")
AddRelTag(fixer, $lineStyle=DottedLine(), $lineColor=$fixer_color)

Person(squad, "Unicorn Squad", "Software engineering, Git and CI/CD experts, using purple horn magic to maintain legacy code", $tags="unicorns", $sprite=unicornSprite)
Container(legacy_code, "Legacy Code Noodles", "Yakisoba", "Legacy code in the form of deep fried soba noodles", $tags="legacy", $sprite=gitSprite)

Rel(squad, legacy_code, "Fixing everything", "Horn magic")

LAYOUT_WITH_LEGEND()
SHOW_LEGEND()
@enduml
```

![example](https://raw.githubusercontent.com/andecy64/plantuml-aws-color-palette/master/examples/unicorns.png)

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
