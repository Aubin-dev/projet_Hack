<template>
  <div>
    <!-- Commencez à coder ici -->
    <div class="container">
        <nav class="navbar">
            <div class="navbar-icon">
            </div>
            <div class="navbar-left">
                <nuxt-link to=""></nuxt-link>
                <nuxt-link to=""></nuxt-link>
                <nuxt-link class="active_link" to=""></nuxt-link>
            </div>
            <div class="navbar-right">
                <nuxt-link to=""></nuxt-link>
                <nuxt-link to=""></nuxt-link>
                <nuxt-link to="">
                    <img width="30" src="#" alt="avatar">
                </nuxt-link>
                <div class="sidelist disp-flex" @click="logOut">
            <nuxt-link to="/login">
                <button class="btn-none">Deconnexion</button>
            </nuxt-link>
            </div>
            </div>
        </nav>
        <main>
            <div class="main-container">
                <div class="main-title">
                    <div class="main-greeting">
                        <h1> Hello {{userData.name}}</h1>
                        <p>Welcome to your admin dashboard </p>
                    </div>
                </div>
                <div class="main-cards">

                    <div class="card">
                        <div class="card-inner">
                            <p class="text-primary-p">Nombre de documents</p>
                            <span class="font-bold text-title">578</span>
                        </div>
                    </div>

                    <div class="card">
                        <div class="card-inner">
                            <p class="text-primary-p">Documents signés</p>
                            <span class="font-bold text-title">340</span>
                        </div>
                    </div>

                    <div class="card">
                        <div class="card-inner">
                            <p class="text-primary-p">Documents non signés</p>
                            <span class="font-bold text-title">248</span>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-inner">
                            <p class="text-primary-p">Autres</p>
                            <span class="font-bold text-title">248</span>
                        </div>
                    </div>
                </div>
            </div>
        </main>
        <div id="sidebar">
            <div class="sidebar__title">
                 <div class="logo">
                    <h1>
                        <nuxt-link to="/">Sign</nuxt-link>
                    </h1>
                </div>
                <i onclick="closeSidebar()" class="fa fa-times" id="sidebarIcon" aria-hidden="true"></i>
            </div>

            <div class="sidebar__menu">
                <div class="sidebar__link active_menu_link">
                    <i class="fa fa-home"></i>
                    <a href="#">Dashboard</a>
                </div>
                <h2>MNG</h2>
                <div class="sidebar__link">
                    <i class="fa fa-user-s¬œecret" aria-hidden="true"></i>
                    <a href="#">Admin Management</a>
                </div>
                <div class="sidebar__link">
                    <i class="fa fa-building-o"></i>
                    <a href="#">Company Management</a>
                </div>
                <div class="sidebar__link">
                    <i class="fa fa-wrench"></i>
                    <a href="#">Employee Management</a>
                </div>
                <div class="sidebar__link">
                    <i class="fa fa-archive"></i>
                    <a href="#">Documents</a>
                </div>
                <div class="sidebar__link">
                    <i class="fa fa-handshake-o"></i>
                    <a href="#">Contracts</a>
                </div>
                <div class="sidebar__link">
                    <i class="fa fa-calendar-check-o"></i>
                    <a href="#">Special Days</a>
                </div>
                <div class="sidebar__link">
                    <i class="fa fa-files-o"></i>
                    <a href="#">Apply for leave</a>
                </div>
                <h2>PAYROLL</h2>
                <div class="sidebar__link">
                    <i class="fa fa-money"></i>
                    <a href="#">Payroll</a>
                </div>
            </div>
        </div>
    </div>
        <!-- <div class="container disp-flex"> -->
        <!-- SIDEBAR LEFT -->
        <!-- <div class="sidebar-left">
            <div class="sidelist disp-flex">
            <nuxt-link to="/timeline">
                <img src="~/assets/svg/home.svg" alt="icon" class="icon">
                <button class="btn-none">Accueil</button>
            </nuxt-link>
            </div>
            <div class="sidelist disp-flex">
            <nuxt-link to="/audio">
                <img src="~/assets/svg/audio.svg" alt="icon" class="icon">
                <button class="btn-none">Mes audios</button>
            </nuxt-link>
            </div>
            <div class="sidelist disp-flex">
            <nuxt-link to="/profil">
                <img src="~/assets/svg/user.svg" alt="icon" class="icon">
                <button class="btn-none">Profil</button>
            </nuxt-link>
            </div>
            <div class="sidelist disp-flex">
            <nuxt-link to="/post">
                <img src="~/assets/svg/post.svg" alt="icon" class="icon">
                <button class="btn-none">Publier</button>
            </nuxt-link>
            </div>
            <div class="sidelist disp-flex" @click="logOut">
            <nuxt-link to="/login">
                <button class="btn-none">Se déconnecter</button>
            </nuxt-link>
            </div>
        </div> -->
        <!-- CONTENU PRINCIPAL -->
        <!-- <div class="user-contain">
            <div class="content-overlay" v-show="loading">
            <img src="~/assets/svg/oval.svg" alt="">
            </div>
            <div class="profil-content">
            <div class="profil-cover">
                <div class="icon-edit-banner" @click="bannerForm">
                <img src="~/assets/svg/edit.svg" alt="icon" class="icon">
                </div>
                <img :src="`http://localhost:5001/uploads/images/${userData.banner}`" alt="story-cover" class="usercov">
            </div>
            <div class="circle big-circle">
                <div class="icon-edit-profilpic" @click="profilpicForm">
                <img src="~/assets/svg/edit.svg" alt="icon" class="icon">
                </div>
                <img :src="`http://localhost:5001/uploads/images/${userData.profilpic}`" alt="user" class="user">
            </div>
            <div class="identity">
                <p class="username">{{ userData.profilname }}</p>
                <p class="pseudo">@{{ userData.pseudo }}</p>
            </div>
            <div class="descrip">
                <span>{{ userData.bio }}</span>
            </div>
            <div class="box-button">
                <button class="btn" @click="updateForm">Editer profil</button>
            </div>
            </div> -->
            <!-- EDIT PROFIL -->
            <!-- <div class="edit-form" v-show="showUpdateForm">
            <div class="update-profil">
                <div class="header">
                <button @click="updateForm">
                    <img src="~/assets/svg/close-btn.svg" alt="icon" class="icon">
                </button>
                <h2>Modifier le profil</h2>
                </div>
                <form action="/user" method="POST">
                <div class="label">
                    <span>Nom de profil</span>
                    <input v-model="username" type="text" name="username" autocomplete="off">
                </div>
                <div class="label">
                    <span>Pseudo</span>
                    <input v-model="pseudo" type="text" name="pseudo" autocomplete="off">
                </div>
                <div class="label">
                    <span>Biograghie</span>
                    <input v-model="bio" type="text" name="bio" autocomplete="off">
                </div>
                <button type="submit" @click="updateUserInfo">
                    Modifier
                </button>
                </form>
            </div>
            </div> -->
            <!-- EDIT PROFIL PIC -->
            <!-- <div class="edit-prodilpic" v-show="showProfilpicForm">
            <div class="update-banner">
                <div class="header">
                <button @click="profilpicForm">
                    <img src="~/assets/svg/close-btn.svg" alt="icon" class="icon">
                </button>
                <h2>Modifier la photo de profil</h2>
                </div>
                <form action="/user" method="POST">
                <div class="label">
                    <span>Photo de profil</span>
                    <input @change="processFile($event)" type="file" name="profilpic" id="profilpic">
                </div>
                <button type="submit" @click="updateProfilPic">Modifier</button>
                </form>
            </div>
            </div> -->
        <!-- </div>
        </div> -->
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data () {
    return {
      loading: true,
      userData: '',
      userPost: '',
      showUpdateForm: false,
      showBannerForm: false,
      showProfilpicForm: false,
      username: '',
      pseudo: '',
      bio: '',
      photo: '',
      modifResponse: '',
      indexPost: '',
      audio: ''
    }
  },
  async mounted () {
    setTimeout(() => {
      this.loading = false
    }, 2000)
    const userId = localStorage.getItem('userId')
    if (userId) {
      // Fetch user info
      this.userData = await axios.get(`http://localhost:5001/api/user/${userId}`)
        .then((res) => {
          return res.data
        })
        .catch(function (err) {
          return err
        })
      // Fetch user post
      this.userPost = await axios.get(`http://localhost:5001/api/user/post/${userId}`)
        .then((res) => {
          return res.data
        })
        .catch(function (err) {
          return err
        })
    } else {
      this.$router.push('/login')
    }
  },
  methods: {
    logOut () {
      localStorage.removeItem('userId')
      this.$router.push('/login')
    },
    updateForm () {
      this.showUpdateForm = !this.showUpdateForm
    },
    processFile (event) {
      this.photo = event.target.files[0]
    },
    async updateUserInfo (e) {
      e.preventDefault()
      const userId = localStorage.getItem('userId')
      const data = {
        id: userId,
        name: this.name
      }
      await axios({ method: 'post', url: 'http://localhost:5001/api/user/update', data })
      this.showUpdateForm = !this.showUpdateForm
      this.username = ''
      this.pseudo = ''
      this.bio = ''
      this.loading = true
      this.userData = await axios.get(`http://localhost:5001/api/user/${userId}`)
        .then((res) => {
          return res.data
        })
        .catch(function (err) {
          return err
        })
      setTimeout(() => {
        this.loading = false
      }, 2000)
    },
    async updateBanner (e) {
      e.preventDefault()
      const userId = localStorage.getItem('userId')
      const file = this.photo
      const formData = new FormData()
      formData.append('file', file)
      await axios({ method: 'post', url: `http://localhost:5001/api/user/upload/banner/${userId}`, data: formData, headers: { 'Content-Type': 'multipart/form-data' } })
      this.showBannerForm = !this.showBannerForm
      this.loading = true
      this.photo = ''
      this.userData = await axios.get(`http://localhost:5001/api/user/${userId}`)
        .then((res) => {
          return res.data
        })
        .catch(function (err) {
          return err
        })
      setTimeout(() => {
        this.loading = false
      }, 2000)
    },
    async updateProfilPic (e) {
      e.preventDefault()
      const userId = localStorage.getItem('userId')
      const file = this.photo
      const formData = new FormData()
      formData.append('file', file)
      await axios({ method: 'post', url: `http://localhost:5001/api/user/upload/profilpic/${userId}`, data: formData, headers: { 'Content-Type': 'multipart/form-data' } })
      this.showProfilpicForm = !this.showProfilpicForm
      this.loading = true
      this.photo = ''
      this.userData = await axios.get(`http://localhost:5001/api/user/${userId}`)
        .then((res) => {
          return res.data
        })
        .catch(function (err) {
          return err
        })
      setTimeout(() => {
        this.loading = false
      }, 2000)
    }
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&display=swap");
/*  styling scrollbars  */
::-webkit-scrollbar {
    width: 5px;
    height: 6px;
}

::-webkit-scrollbar-track {
    box-shadow: inset 0 0 5px #a5aaad;
    border-radius: 10px;
}

::-webkit-scrollbar-thumb {
    background: #3ea175;
    border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
    background: #a5aaad;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.text-primary-p {
    color: #a5aaad;
    font-size: 14px;
    font-weight: 700;
}

.font-bold {
    font-weight: 700;
}

.text-title {
    color: #2e4a66;
}

.text-lightblue {
    color: #469cac;
}

.text-red {
    color: #cc3d38;
}

.text-yellow {
    color: #a98921;
}

.text-green {
    color: #3b9668;
}

a{
  text-decoration: none;
}
.navbar {
    background: #ffffff;
    grid-area: nav;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 30px 0 30px;
    border-bottom: 1px solid lightgray;
}

.container{
   display: grid;
    height: 100vh;
    grid-template-columns: 0.8fr 1fr 1fr 1fr;
    grid-template-rows: 0.2fr 3fr;
    grid-template-areas:
        "sidebar nav nav nav"
        "sidebar main main main";
}
.navbar-left > a {
    margin-right: 30px;
    text-decoration: none;
    color: #a5aaad;
    font-size: 15px;
    font-weight: 700;
}

.navbar-left .active_link {
    color: #265acc;
    border-bottom: 3px solid #265acc;
    padding-bottom: 12px;
}
.desktop-menu{
    position: relative;
    width:100%;
}

.menu-items {
    position: relative;
    width: 100%;
    right:0;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.navbar-right{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.navbar-right > a {
    margin-left: 20px;
    text-decoration: none;
}

.navbar-right > a > i {
    color: #a5aaad;
    font-size: 16px;
    border-radius: 50px;
    background: #ffffff;
    box-shadow: 2px 2px 5px #d9d9d9, -2px -2px 5px #ffffff;
    padding: 7px;
}

main {
    background: #f3f4f6;
    grid-area: main;
    overflow-y: auto;
}

.main-container {
    padding: 20px 35px;
    margin-top: 25px;
    display: block;

}

.main-title {
    display: flex;
    align-items: center;
    margin-top: 15px;
}

.main-title > img {
    max-height: 100px;
    object-fit: contain;
    margin-right: 20px;
}

.main-greeting > h1 {
    font-size: 24px;
    color: #2e4a66;
    margin-bottom: 5px;
}

.main-greeting > p {
    font-size: 14px;
    font-weight: 700;
    color: #a5aaad;
}
.main-cards {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 30px;
    margin: 50px 0;
}

.card {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    height: 70px;
    padding: 25px;
    border-radius: 5px;
    background: #ffffff;
    box-shadow: 5px 5px 13px #ededed, -5px -5px 13px #ffffff;
}

.card-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.card-inner > span {
    font-size: 25px;
}

.charts {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 30px;
    margin-top: 50px;
}
.charts-left{
    padding: 25px;
}

.charts-left-title {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.charts-left-title > div > h1 {
    font-size: 24px;
    color: #2e4a66;
    margin-bottom: 5px;
}

.charts-left-title > div > p {
    font-size: 14px;
    font-weight: 700;
    color: #a5aaad;
}

.charts-left-title > i {
    color: #ffffff;
    font-size: 20px;
    background: #ffc100;
    border-radius: 200px 0px 200px 200px;
    -moz-border-radius: 200px 0px 200px 200px;
    -webkit-border-radius: 200px 0px 200px 200px;
    border: 0px solid #000000;
    padding: 15px;
}

.charts__right {
    padding: 25px;
    border-radius: 5px;
    background: #ffffff;
    box-shadow: 5px 5px 13px #ededed, -5px -5px 13px #ffffff;
}

.charts__right__title {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.charts__right__title > div > h1 {
    font-size: 24px;
    color: #2e4a66;
    margin-bottom: 5px;
}

.charts__right__title > div > p {
    font-size: 14px;
    font-weight: 700;
    color: #a5aaad;
}

.charts__right__title > i {
    color: #ffffff;
    font-size: 20px;
    background: #39447a;
    border-radius: 200px 0px 200px 200px;
    -moz-border-radius: 200px 0px 200px 200px;
    -webkit-border-radius: 200px 0px 200px 200px;
    border: 0px solid #000000;
    padding: 15px;
}
.charts__right__cards {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin-top: 30px;
}

.card1 {
    background: #d1ecf1;
    color: #35a4ba;
    text-align: center;
    padding: 25px;
    border-radius: 5px;
    font-size: 14px;
}

.card2 {
    background: #d2f9ee;
    color: #38e1b0;
    text-align: center;
    padding: 25px;
    border-radius: 5px;
    font-size: 14px;
}

.card3 {
    background: #d6d8d9;
    color: #3a3e41;
    text-align: center;
    padding: 25px;
    border-radius: 5px;
    font-size: 14px;
}

.card4 {
    background: #fddcdf;
    color: #f65a6f;
    text-align: center;
    padding: 25px;
    border-radius: 5px;
    font-size: 14px;
}

#sidebar {
    background: #2e3a49;
    grid-area: sidebar;
    overflow-y: auto;
    padding: 20px;
    -webkit-transition: all 0.5s;
    transition: all 0.5s;
}

.sidebar__title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #f3f4f6;
    margin-bottom: 30px;
}

.sidebar__img {
    display: flex;
    align-items: center;
}

.sidebar__title > div > img {
    width: 75px;
    object-fit: contain;

}

.sidebar__title > div > h1 {
    font-size: 18px;
    display: inline;
    cursor: pointer;
}

.sidebar__title > i {
    font-size: 18px;
    display: none;
}
.sidebar__menu > h2 {
    color: #3ea175;
    font-size: 16px;
    margin-top: 15px;
    margin-bottom: 5px;
    padding: 0 10px;
    font-weight: 700;
}

.sidebar__link {
    color: #f3f4f6;
    padding: 10px;
    border-radius: 3px;
    margin-bottom: 5px;
}

.active_menu_link {
    background: rgba(62, 161, 117, 0.3);
    color: #3ea175;
}

.active_menu_link a {
    color: #3ea175 !important;
}

.sidebar__link > a {
    text-decoration: none;
    color: #a5aaad;
    font-weight: 700;
}

.sidebar__link > i {
    margin-right: 10px;
    font-size: 18px;
}

.sidebar_responsive {
    display: inline !important;
    z-index: 9999 !important;
    left: 0 !important;
    position: absolute;
}
@media only screen and (max-width: 978px) {
    .container {
        grid-template-columns: 1fr;
      /* grid-template-rows: 0.2fr 2.2fr; */
        grid-template-rows: 0.2fr 3fr;
        grid-template-areas:
        "nav"
        "main";
    }
    #sidebar {
        display: none;
    }
    .sidebar__title > i {
        display: inline;
    }
    .navbar-icon {
        display: inline;
    }
}

@media only screen and (max-width: 855px) {
    .main-cards {
        grid-template-columns: 1fr;
        gap: 10px;
        margin-bottom: 0;
    }
    .charts {
        grid-template-columns: 1fr;
        margin-top: 30px;
    }
}

@media only screen and (max-width: 480px) {
    .navbar__left {
        display: none;
    }
}

</style>
