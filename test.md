### Model Hiearchy
```
@startuml
class Model <-- PredictiveModel
PredictiveModel <-- MLModel
PredictiveModel <-- BooleanModel
PredictiveModel <-- RuleBasedModel
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
