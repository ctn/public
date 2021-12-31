## General Design
```
@startuml
interface Modelable
Modeler - Modelable : produces >
Model ..> Modelable : implements
@enduml
```

### Examples

```
@startuml
interface Modelable
MLModeler - Modelable : produces >
MLModel ..> Modelable : implements
@enduml

```
