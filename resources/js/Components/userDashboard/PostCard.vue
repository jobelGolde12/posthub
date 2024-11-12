<template>
    <div class="main-container">
                    <div class="ad-container shadow-sm container">
            <!-- Header -->
            <div class="ad-header">
                <div class="profile-pic"></div>
                <div>
                <strong>daily.dev</strong> <span class="text-muted">Sponsored</span>
                <div class="text-muted" style="font-size: 12px;">Try it now its free!</div>
                </div>
                <div class="ms-auto text-muted">⋮</div>
            </div>

            <!-- Content -->
            <div class="ad-content">
                <p class="mt-3 mb-0"><strong>Try it now its free!</strong></p>
                <p class="text-muted">Are you a developer?! Stay up to date, research, f...</p>
                <a href="#" class="btn-learn-more">Learn more</a>
                <img src="https://via.placeholder.com/500x250.png?text=Website+Screenshot" alt="Website Screenshot">
            </div>

            <!-- Footer with Reactions -->
            <div class="ad-footer">
                <div class="reactions mb-2">
                <div class="reaction-icons">
                    <img src="https://via.placeholder.com/20x20.png?text=👍" alt="like">
                    <img src="https://via.placeholder.com/20x20.png?text=❤️" alt="love">
                    <span class="text-muted ms-2">874</span>
                </div>
                <div class="text-muted">38 Comments · 51 Shares</div>
                </div>
                
                <!-- Action Buttons -->
                <div class="action-buttons">
                <div class="action-button">
                    <img src="https://via.placeholder.com/20x20.png?text=👍" alt="Like">
                    <span>Like</span>
                </div>
                <div class="action-button">
                    <img src="https://via.placeholder.com/20x20.png?text=💬" alt="Comment">
                    <span>Comment</span>
                </div>
                <div class="action-button">
                    <img src="https://via.placeholder.com/20x20.png?text=↗" alt="Share">
                    <span>Share</span>
                </div>
                </div>
            </div>
            </div>

    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="css" scoped>
    /* .main-container{
        position: absolute;
        width: 100%;
        height: 100%;
    } */
    .ad-container {
      /* max-width: 640px;
      max-height: 500px; */
      border: 1px solid #ddd;
      border-radius: 8px;
      margin: 20px auto;
      background-color: #fff;
      font-family: Arial, sans-serif;

    }
    .ad-header, .ad-footer {
      padding: 10px 16px;
    }
    .ad-header {
      display: flex;
      align-items: center;
      border-bottom: 1px solid #ddd;
    }
    .profile-pic {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background-color: #ccc;
      margin-right: 10px;
    }
    .ad-content {
      padding: 16px;
      text-align: center;
    }
    .ad-content img {
      max-width: 100%;
      border-radius: 8px;
    }
    .btn-learn-more {
      background-color: #1c6ede;
      color: #fff;
      font-weight: bold;
      border-radius: 6px;
      padding: 8px 16px;
      text-decoration: none;
      display: inline-block;
      margin-top: 10px;
    }
    .reactions, .comments {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .reaction-icons {
      display: flex;
      align-items: center;
    }
    .reaction-icons img {
      width: 20px;
      margin-right: 4px;
    }
    .action-buttons {
      display: flex;
      justify-content: space-around;
      padding: 8px 0;
      border-top: 1px solid #ddd;
      border-bottom: 1px solid #ddd;
    }
    .action-button {
      display: flex;
      align-items: center;
      font-size: 14px;
      color: #606770;
    }
    .action-button img {
      width: 20px;
      margin-right: 8px;
    }
</style>