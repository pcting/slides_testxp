## Hard to Test Example
<br />
    public class EntityController {

      IRepo repo = new EntityRepo(...);

      public Entity find(int id) {
        Date d = Date.now();
        if (d.getTime() % 60000 >= 30000) {
          return repo.getEntity(id, d);
        } else {
          return null;
        }
      }

    }
