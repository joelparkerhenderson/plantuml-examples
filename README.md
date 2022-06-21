# PlantUML demo

PlantUML is a tool that uses text formatting to create graphic diagrams. See http://plantuml.com

Contents:

- [PlantUML demo](#plantuml-demo)
  - [Sequence diagram demo](#sequence-diagram-demo)
  - [Sequence diagram demo with steps and divider](#sequence-diagram-demo-with-steps-and-divider)
  - [Usecase diagram demo](#usecase-diagram-demo)
  - [Object diagram demo](#object-diagram-demo)
  - [Class diagram demo](#class-diagram-demo)
  - [Package styles](#package-styles)
  - [Activity diagram demo](#activity-diagram-demo)
  - [Component diagram demo of items](#component-diagram-demo-of-items)
  - [State diagram demo](#state-diagram-demo)
  - [Deployment diagram demo of items](#deployment-diagram-demo-of-items)
  - [Timing diagram demo](#timing-diagram-demo)
  - [Wireframe demo](#wireframe-demo)
  - [Gantt chart demo](#gantt-chart-demo)
  - [Font Awesome demo](#font-awesome-demo)
  - [Procedure demo](#procedure-demo)
  - [Area diagram demo](#area-diagram-demo)


## Sequence diagram demo

![Sequence diagram](doc/sequence_diagram/sequence_diagram.png)

```plantuml
@startuml
skinparam monochrome true
Alpha -> Bravo
Bravo -> Alpha
@enduml
```


## Sequence diagram demo with steps and divider

![Sequence diagram extras](doc/sequence_diagram_extras/sequence_diagram_extras.png)

```plantuml
@startuml
skinparam monochrome true
Alpha -> Bravo: Step 1
Bravo -> Charlie: Step 2
== My Divider ==
Charlie -> Bravo: Step 3
Bravo -> Alpha: Step 4
@enduml
```

## Usecase diagram demo

![Usecase diagram](doc/usecase_diagram/usecase_diagram.png)

```plantuml
@startuml
skinparam monochrome true
left to right direction
User1 --> (Story1)
(Story1) --> (Story2)
(Story2) --> (Story3)
@enduml
```


## Object diagram demo

![Object diagram](doc/object_diagram/object_diagram.png)

```plantuml
@startuml
skinparam monochrome true
object Object1 {
  Alpha
  Bravo
  Charlie
}
object Object2 {
  Delta
  Echo
  Foxtrot
}
object Object3 {
  Golf
  Hotel
  Indigo
}
object Object4 {
  Juliet
  Kilo
  Lima
}
Object1 <|-- Object2
Object1 *-- Object3
Object1 o-- Object4
@enduml
```

## Class diagram demo

![Class diagram](doc/class_diagram/class_diagram.png)

```plantuml
@startuml
skinparam monochrome true
class Class1 {
  {field} Alpha
  {method} Bravo
  {method} Charlie
}
class Class2 {
  {field} Delta
  {method} Echo
  {method} Foxtrot
}
class Class3 {
  {field} Golf
  {method} Hotel
  {method} Indigo
}
class Class4 {
  {field} Juliet
  {method} Kilo
  {method} Lima
}
Class1 <|-- Class2
Class1 *-- Class3
Class1 o-- Class4
@enduml
```

## Package styles

![Package styles](doc/package_styles/package_styles.png)

```
@startuml
package "Demo Node" <<Node>> {
  object Object1
}
package "Demo Rectangle" <<Rectangle>> {
  object Object2
}
package "Demo Folder" <<Folder>> {
  object Object3
}
package "Demo Frame" <<Frame>> {
  object Object4
}
package "Demo Cloud" <<Cloud>> {
  object Object5
}
package "Demo Database" <<Database>> {
  object Object6
}
@enduml
```


## Activity diagram demo

![Activity diagram](doc/activity_diagram/activity_diagram.png)

```plantuml
@startuml
skinparam monochrome true
start
-> Starting;
:Activity 1;
if (Question) then (yes)
  :Option 1;
else (no)
  :Option 2;
endif
:Activity 2;
-> Stopping;
stop
@enduml
```


## Component diagram demo of items

![Component diagram](doc/component_diagram/component_diagram.png)

```plantuml
@startuml
skinparam monochrome true
component "Component"
interface "Interface"
database "Database"
cloud "Cloud"
node "Node"
package "Package"
@enduml
```


## State diagram demo

![State diagram](doc/state_diagram/state_diagram.png)

```plantuml
@startuml
skinparam monochrome true
[*] --> State1 : Start
State1 -> State2 : Change1
State2 -> State3 : Change2
State3 --> [*] : Stop
State1 : Description 1
State2 : Description 2
State3 : Description 3
@enduml
```


## Deployment diagram demo of items

![Deployment diagram](doc/deployment_diagram/deployment_diagram.png)

```plantuml
@startuml
skinparam monochrome true
actor actor
agent agent
artifact artifact
boundary boundary
card card
cloud cloud
component component
control control
database database
entity entity
file file
folder folder
frame frame
interface  interface
node node
package package
queue queue
stack stack
rectangle rectangle
storage storage
usecase usecase
@enduml
```


## Timing diagram demo

![Timing diagram](doc/timing_diagram/timing_diagram.png)

```plantuml
@startuml
skinparam monochrome true
concise "My Timeline" as T
@T
0 is Alpha
+100 is Bravo
+100 is Charlie
@50 <-> @+100 : My Note
@enduml
```


## Wireframe demo

![Wireframe](doc/wireframe/wireframe.png)

```plantuml
@startuml
salt
{
  Hello world
  [Button]
  ()  Radio 1
  (X) Radio 2
  []  Checkbox 1
  [X] Checkbox 2
  "Enter text here   "
  ^This is a droplist^
}
@enduml
```


## Gantt chart demo

![Gantt chart](doc/gantt_chart/gantt_chart.png)

```plantuml
@startgantt
skinparam monochrome true
[Task1] on {Alice} lasts 8 days
then [Task2] on {Bob} lasts 4 days at 50%
then [Task3] on {Carol} lasts 2 days at 25%
@endgantt
```

## Font Awesome demo

![Font Awesome](doc/font_awesome/font_awesome.png)

```plantuml
@startuml
skinparam monochrome true
!include <font-awesome/star>
rectangle "<$star>"
@enduml
```


## Procedure demo

![Procedure diagram](doc/procedure/procedure.png)

```plantuml
@startuml
!procedure $demo($name, $headline, $description)
  card $name as "\n<size:22>$headline</size>\n\n<size:12>$description</size>\n"
!endprocedure
$demo(MyCard, "Hello World", "This is a demonstration")
@enduml
```


## Area diagram demo

![Area diagram](doc/area_diagram/area_diagram.png)

[Area diagram PlantUML](doc/area_diagram/area_diagram.txt)

The area diagram is an example deployment diagram that shows a bunch of areas and how they interrlate. This example is useful for seeing a real-world diagram, that uses boxes, arrows, Font Awesome icons, multi-line text, Unicode padding, font sizes, and more.
