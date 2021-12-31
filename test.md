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
Modelable <.. Model : implements
Modeler - Modelable : produces >
@enduml
```

### Oracle (Model)
```
@startuml
class Oracle
MLModel <-- Oracle
Oracle o-- Ensemble
Ensemble <.. Teacher
Ensemble <.. Student
Oracle o-- Teacher
Oracle o-- Student
@enduml
```
