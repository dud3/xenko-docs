# Entity-Component Model

# Overview

@'SiliconStudio.Xenko.EntityModel.Entity' is the base class for objects that are managed by the high-level engine.

To improve flexibility, entity are component-based: they can contains as many components as required, containing data and/or logic.




![images/7438980.png](images/7438980.png) 




A @'SiliconStudio.Xenko.EntityModel.Entitycomponent' is tied to its entity (that is, one component can't be added to two entities at the same time).

# How to create an entity and some components

```cs
// Create entity
var myEntity = new Entity();
 
// Create a model component (so that model is rendered)
var modelComponent = new ModelComponent { Model = model };
myEntity.Set(ModelComponent.Key, modelComponent);

// Set entity position
myEntity.Transformation.Translation = new Vector3(100.0f, 100.0f, 0.0f);
 
// Add entity to scene; from now on its model will be rendered
Entities.Add(myEntity);
```


