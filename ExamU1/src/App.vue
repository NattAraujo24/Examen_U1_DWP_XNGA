 <template>
  <b-container fluid>
    <b-row>
      <b-col>
        <div>
          <b-navbar toggleable="lg" type="dark" variant="dark" fixed="top">
            <b-navbar-brand href="#">NavBar</b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
              <b-navbar-nav>
                <b-nav-item href="#">Link</b-nav-item>
                <b-nav-item href="#" disabled>Disabled</b-nav-item>
              </b-navbar-nav>
              <b-navbar-nav class="ml-auto">
                <b-nav-item-dropdown right>
                  <template #button-content>
                    <em>User</em>
                  </template>
                  <b-dropdown-item href="#">Profile</b-dropdown-item>
                  <b-dropdown-item href="#">Sign Out</b-dropdown-item>
                </b-nav-item-dropdown>
              </b-navbar-nav>
            </b-collapse>
          </b-navbar>
        </div>
      </b-col>
    </b-row>

    
    <b-row>
      <b-col>
        <div>
          <b-sidebar id="sidebar-1" title="Sidebar" shadow visible z-index="0" no-close-on-backdrop no-close-on-esc no-close-on-route-change>
            <div class="px-3 py-2">
              <b-nav-item>
                <b-link :to="{name: 'inicio'}">
                  Inicio
                </b-link>
              </b-nav-item>
              <b-nav-item>
                <b-link :to="{name: 'formulario'}">
                  Formulario
                </b-link>
              </b-nav-item>
              <b-nav-item>
                <b-link :to="{name: 'paginacion'}">
                  Paginacion
                </b-link>
              </b-nav-item>
            </div>
          </b-sidebar>
        </div>
      </b-col>
      <b-col>
        <router-view></router-view>
      </b-col>
    </b-row>
  </b-container>
</template>
<script>
 export default {
    data() {
      return {
        items: [
          {
            text: 'Inicio',
            href: '#',
            to:"formulario"
          },
          {
            text: 'Formulario',
            href: '#',
            to: "paginacion"
          },
          {
            text: 'Paginacion',
            href: '#',
            to: "inicio"
          },
        ]
      }
    }
  }
</script>