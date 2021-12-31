### Model Hiearchy
```
@startuml
Model <|-- PredictiveModel <|-- MLModel
@enduml
```

### Modelable
```
@startuml
interface Modelable
Modeler - Modelable : produces >
Model ..> Modelable : implements
@enduml
```

```
@startuml
interface Modelable
MLModeler - Modelable : produces >
MLModel ..> Modelable : implements
@enduml

```
