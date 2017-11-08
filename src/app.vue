<template>
  <!-- App -->
  <div id="app">

    <!-- Statusbar -->
    <!-- <f7-statusbar></f7-statusbar> -->

    <!-- Left Panel -->
    <f7-panel left reveal layout="white">
      <f7-view id="left-panel-view" navbar-through :dynamic-navbar="true">
        <f7-navbar v-if="$theme.ios" title="Left Panel" sliding></f7-navbar>
        <f7-pages>
          <f7-page>
            <f7-navbar v-if="$theme.material" title="Left Panel" sliding></f7-navbar>
            <f7-block inner>
              <p>Left panel content goes here</p>
            </f7-block>
            <f7-block-title>Load page in panel</f7-block-title>
            <f7-list>
              <f7-list-item link="/about/" title="About"></f7-list-item>
              <f7-list-item link="/form/" title="Form"></f7-list-item>
            </f7-list>
            <f7-block-title>Load page in main view</f7-block-title>
            <f7-list>
              <f7-list-item link="/about/" title="About" link-view="#main-view" link-close-panel></f7-list-item>
              <f7-list-item link="/form/" title="Form" link-view="#main-view" link-close-panel></f7-list-item>
            </f7-list>
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-panel>


    <!-- Main Views -->
    <f7-views>
      <f7-view id="main-view" navbar-through :dynamic-navbar="true" main>
        <!-- iOS Theme Navbar -->
        <!-- Pages -->
        <f7-pages>
          <f7-page>
        <f7-navbar>
          <f7-nav-left>
            <f7-link icon="icon-bars" open-panel="left"></f7-link>
          </f7-nav-left>
          <f7-nav-center sliding>My App</f7-nav-center>
          <f7-nav-right>
          </f7-nav-right>

        </f7-navbar>
            <!-- Material Theme Navbar -->
            <!-- <f7-navbar v-if="$theme.material">
              <f7-nav-left>
                <f7-link icon="icon-bars" open-panel="left"></f7-link>
              </f7-nav-left>
              <f7-nav-center sliding>Framework7</f7-nav-center>
            </f7-navbar> -->
            <!-- Page Content -->
            <f7-block-title>Welcome to my App</f7-block-title>
            <f7-block inner>
              <p>Duis sed erat ac eros ultrices pharetra id ut tellus. Praesent rhoncus enim ornare ipsum aliquet ultricies. Pellentesque sodales erat quis elementum sagittis.</p>
            </f7-block>
            <f7-block-title>Navigation</f7-block-title>
            <f7-list>
              <f7-list-item link="/about/" title="About"></f7-list-item>
              <f7-list-item link="/form/" title="Form"></f7-list-item>
              <f7-list-item link="/dynamic-route/blog/45/post/125/?foo=bar#about" title="Dynamic Route"></f7-list-item>
            </f7-list>
            <f7-block-title>下面是按钮</f7-block-title>
            <f7-buttons>
              <f7-button @click="$router.load({url: '/about/'})" link-view="#main-view"  >about</f7-button>
              <f7-button @click="$router.load({url: '/form/'})" >form</f7-button>
              <f7-button @click="$router.load({url: '/dynamic-route/blog/45/post/125/?foo=bar#about'})" >dynamic-route</f7-button>
              
            </f7-buttons> 
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-views>




  </div>
</template>

<script>
export default {}
</script>