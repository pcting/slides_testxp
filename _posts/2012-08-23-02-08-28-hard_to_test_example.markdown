## Hard to Test Example
<br />
    public class EntityController {

      IRepo repo = new EntityRepo(...);

      public Entity find(int id) {
        Date d = Date.now();
        return repo.getEntity(id, d);
      }

    }
