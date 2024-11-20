<template>
    <div class="app">
      <!-- Main header -->
      <h1>My Cashflow Tracker</h1>
  
      <!-- User Profile Section -->
      <div class="user-profile">
        
        <!-- Profile Picture -->
        <div class="profile-picture">
          <img :src="user.profilePicture" alt="User's profile picture" />
        </div>
  
        <!-- User Info -->
        <div class="user-info">
          <p><strong>Name:</strong> {{ user.name }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        // User data
        user: {
          profilePicture: 'https://res.cloudinary.com/dreos8j8v/image/upload/w_1000,c_fill,ar_1:1,g_auto,r_max,bo_5px_solid_red,b_rgb:262c35/v1731141460/Admin_yxo01n.jpg', // Default profile picture
          name: 'NickDevOps',
        }
      };
    }
  }
  </script>
  
  <style scoped>
  .app {
    text-align: center;
    padding: 20px;
  }

  
  /* Profile picture styles */
  .profile-picture {
    text-align: center;
    margin-bottom: 10px;
  }
  
  .profile-picture img {
    border-radius: 50%;
    width: 80px;
    height: 80px;
    object-fit: cover;
  }
  
  /* User info text styles */
  .user-info p {
    font-size: 16px;
    margin: 5px 0;
    color: #333;
  }
  
  /* Header styles */
  h1 {
    color: #333;
  }
  
  h2 {
    color: #555;
    margin-bottom: 15px;
  }
  
  /* Mobile responsiveness */
  @media (max-width: 768px) {
    /* Make the profile box smaller */
    .user-profile {
      width: 200px;
      top: 10px;
      right: 10px;
      padding: 10px;
    }
  
    /* Resize the profile image */
    .profile-picture img {
      width: 60px;
      height: 60px;
    }
  
    /* Reduce font size for mobile */
    .user-info p {
      font-size: 14px;
    }
  
    /* Adjust header padding for mobile */
    h1 {
      font-size: 20px;
      margin-bottom: 15px;
    }
  }
  
  /* For very small screens (extra mobile-friendly adjustments) */
  @media (max-width: 480px) {
    /* Further reduce profile box size */
    .user-profile {
      width: 180px;
      top: 5px;
      right: 5px;
      padding: 8px;
    }
  
    /* Resize the profile image further */
    .profile-picture img {
      width: 30px;
      height: 30px;
    }
  
    /* Make text smaller on extra small screens */
    .user-info p {
      font-size: 12px;
    }
  
    h1 {
      font-size: 18px;
    }
  }
  </style>
  