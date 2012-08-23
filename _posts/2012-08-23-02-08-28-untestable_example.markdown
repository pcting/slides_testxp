## Untestable Example
<br />
    public class EntityController {

      public Entity find(int id) {
        Date d = Date.now();
        return Entity::getEntity(id, d);
      }

    }
