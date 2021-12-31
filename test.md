### Model Hiearchy
```
@startuml
class Model

Model <-- PredictiveModel
PredictiveModel <-- MLModel
PredictiveModel <-- BooleanModel
PredictiveModel <-- RuleBasedModel
RuleBasedModel <-- FuzzyLogicModel

interface Modelable
Modeler - Modelable : produces >
Model ..> Modelable : implements

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
