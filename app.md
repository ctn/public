*Note: to view these diagrams, install [this Chrome plugin](https://chrome.google.com/webstore/detail/plantuml-visualizer/ffaloebcmkogfdkemcekamlmfkkmgkcf).*

### Model–System (Data Scientist–Software Engineer) Collaboration
```
@startuml
allowmixing
class App
App ..> AppModel : uses
AppModel ..> Model : calls

Actor "Software Engineer" as SWE
Actor "Data Scientist" as DS
SWE ..> App : maintains
Model <.. DS : maintains

together { 
  class App 
  class AppModel 
  class Model 
}
@enduml
```

