*Note: to view these diagrams, install [this Chrome plugin](https://chrome.google.com/webstore/detail/plantuml-visualizer/ffaloebcmkogfdkemcekamlmfkkmgkcf).*

### Model–System (Data Scientist–Software Engineer) Collaboration
```
@startuml
allowmixing
class App
App <.. AppModel : uses

Actor "Software Engineer" as SWE
Actor "Data Scientist" as DS
SWE ..> App : maintains
DS ..> Model : maintains
AppModel ..> Model

together { 
  App 
  class AppModel 
  class Model 
}
@enduml
```

