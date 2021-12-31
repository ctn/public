### Model Hiearchy
```
@startuml
class Model
Model <-- PredictiveModel
PredictiveModel <-- MLModel
PredictiveModel <-- BooleanModel
PredictiveModel <-- RuleBasedModel
RuleBasedModel <-- FuzzyLogicModel
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

### Oracle (Model)
```
@startuml
class Oracle
MLModel <-- Oracle
Oracle o-- Teacher
Oracle o-- Student
Oracle o-- Ensemble
@enduml
```
