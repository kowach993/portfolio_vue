<template>
  <div id="navigation">
    <div id="nav_desktop">
    <div>
    <img id="avatar" src="../assets/avatar.png">
    </div>
    <div id="nav_div">
      <router-link to="/" class="button">Home</router-link>
      <router-link to="/about" class="button">About</router-link>
      <router-link to="/projects" class="button">Projects</router-link>
      <router-link to="/contact" class="button">Contact</router-link>
    </div>
    <div>
      <p id="copy">&copy; Dragan Kovačević 2022</p>
    </div>
    </div>
    <div id="nav_mob">
    <b-icon icon="x-diamond-fill" v-b-toggle.sidebar-backdrop id="b-btn"></b-icon>

    <b-sidebar
      id="sidebar-backdrop"
      backdrop-variant="dark"
      backdrop
      shadow
      text-variant="light"
      title="Menu"
    >
    <div id="mobile_nav">
    <div>
    <img id="avatar" src="../assets/avatar.png">
    </div>
    <div id="nav_div">
      <router-link to="/" class="button">Home</router-link>
      <router-link to="/about" class="button">About</router-link>
      <router-link to="/projects" class="button">Projects</router-link>
      <router-link to="/contact" class="button">Contact</router-link>
    </div>
    <div>
      <p id="copy">&copy; Dragan Kovačević 2022</p>
    </div>
    </div>
    </b-sidebar>
    </div>
    <router-view/>
  </div>
</template>


<script>
export default {
  name: 'navigation'
}
</script>

<style>

.b-sidebar  {
    background-color: #161a1d!important;
}

#mobile_nav, #nav_desktop {
  display: flex;
  align-items: center;
  background-color: #161a1d;
  height: 100%;
  width: 300px;
  flex-direction: column;
}

#nav_div {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

#copy {
  color: #b1a7a6;
}

.button {
  background-color: #b1a7a6;
  border: 1px solid #b1a7a6;
  border-radius: 5px;
  color: white;
  font-size: 18;
  text-align: center;
  margin-bottom: 10px;
}

.button:hover {
  background-color: #e5383b;
  color: white;
  border: 1px solid #e5383b;
}

a.router-link-exact-active {
  background-color: #e5383b;
  color: white;
  border: 1px solid #e5383b;
}

a {
  text-decoration: none!important;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

@media all and (min-width: 577px) and (max-width:991px) {
        #nav_desktop {
          display: none;
        }

        #avatar {
         width: 230px;
          height: 230px;
        }

        .button {
          padding-top: 10px;
          padding-bottom: 10px;
          width: 150px;
        }

        #mobile_nav, #nav_desktop {
          justify-content: space-around;
          }

          #copy {
          position: relative;
          margin-bottom: 200px;
          top: 150px;
        }

        #b-btn {
          position: absolute;
          right: 0;
          color: white;
          font-size: 80px;
          padding: 10px;
        }
}

@media all and (min-width: 992px) {
        #nav_desktop {
            position: absolute;
            }
        #mob_nav, #b-btn {
          display: none;
        }

        .button {
          padding-top: 20px;
          padding-bottom: 20px;
          width: 200px;
        }

         #avatar {
          width: 300px!important;
        }

        #mobile_nav, #nav_desktop {
          justify-content: space-between;
          }
}

@media all and (max-width:576px) {
        #nav_desktop {
          display: none;
        }

        .bg-foobar {
          background-color: #343a40;
          z-index: 2;
        }

        #avatar {
          width: 230px;
          height: 230px;
        }

        .button {
          padding-top: 10px;
          padding-bottom: 10px;
          width: 150px;
        }

        #mobile_nav, #nav_desktop {
          justify-content: space-around;
          }

        #copy {
          position: relative;
          margin-bottom: 200px;
          top: 150px;
        }

        #b-btn {
          position: absolute;
          right: 0;
          color: white;
          font-size: 80px;
          padding: 10px;
        }
}


</style>