## Less Hard to Test Example
<br />
    public class EntityController {

      private IRepo repo;

      // we can perform dependency injection
      public IRepo setRepo(IRepo r) {
        repo = r;
      }

      // we can maintain backwards compatibility
      public Entity find(int id) {
        return find(id, Date.now());
      }

      // ... and still test deterministically
      public Entity find(int id, Date d) {
        return repo.getEntity(id, d);
      }
    }
