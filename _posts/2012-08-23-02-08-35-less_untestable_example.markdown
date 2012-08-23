## Less Untestable Example
<br />
    public class EntityController {
      private IRepo r;
      public IRepo setRepo(IRepo r) {
        this.r = r;
      }
      public Entity find(int id) {
        return find(id, Date.now());
      }
      public Entity find(int id, Date d) {
        return r.getEntity(id, d);
      }
    }
