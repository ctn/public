### Model Hiearchy
```
@startuml
class Model
PredictiveModel <|-- Model
PredictiveModel <|-- MLModel
PredictiveModel <|-- BooleanModel
PredictiveModel <|-- RuleBasedModel
RuleBasedModel <|-- FuzzyLogicModel
@enduml
```

### Modelable
```
@startuml
interface Modelable
Modelable <|.. Model : implements
Modeler - Modelable : produces >
@enduml
```

### Oracle (Model)
```
@startuml
class Oracle
MLModel <|-- Oracle
Oracle o-- Ensemble
Ensemble <.. Teacher
Ensemble <.. Student
EnsembleModeler - Ensemble : produces >
StudentModeler - Student : produces >
user User
User - Teacher : produces >
@enduml
```
