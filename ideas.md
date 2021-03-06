Events:
- entity.remove() => EntityRemoved
- createEntity() => EntityAdded
- entity.addComponent() => query? EntityAddedToQuery
- entity.removeComponent() => query? EntityRemovedFromQuery
  => EntityChanged
- entity.getMutableComponent() => ComponentChanged
  => EntityComponentChanged

- **EntityRemoved(e)** (Cuando la borras directamente la entidad)
- **EntityAdded(e)** (Cuando creas world.createEntity())
- **EntityAddedToQuery(e,c)** (Cuando añades un componente que cumple la condición de la query y la añades)
- **EntityRemovedFromQuery(e,c)** (Cuando eliminas algún componente y ya no cumple las condiciones de la query)
- **EntityChanged(e)** (Cuando cambia alguno de sus componentes, mutate, pero no remove/add)
- **EntityComponentChanged(e,c)** (Cuando cambia un componente en concreto)

- Add 'alive' attribute on components?
- Extend "Component" class for all components
- Limit number of components to 1 on events/queries
- What to do with the Group/Mesh/Object3D if several systems wants to share the same entity
- onEvent attribute on a component to be used for example to trigger the paint/teleport action, how to define it
- this.component inside systems
- async init on systems
- separate between init() and config()/queries()/events()