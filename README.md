<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discord Profile</title>
    <style>
        .profile {
            font-family: Arial, sans-serif;
            max-width: 400px;
            margin: auto;
            text-align: center;
            border: 1px solid #ddd;
            border-radius: 10px;
            padding: 20px;
        }
        .avatar {
            border-radius: 50%;
            width: 100px;
            height: 100px;
        }
        .badges img {
            width: 50px;
            height: 50px;
            margin: 5px;
        }
    </style>
</head>
<body>
    <div class="profile" id="profile">
        <h1>Discord Profile</h1>
        <img src="" alt="Avatar" class="avatar" id="avatar">
        <h2 id="username">Aref But Unstable</h2>
        <div class="badges" id="badges">
            <!-- Lanyard Badges will be inserted here -->
            <!-- Extra Badges -->
            <img src="https://path_to_your_custom_badge/Hype_Squad_Balance.png" alt="Hype Squad Balance">
            <img src="https://path_to_your_custom_badge/Early_Bot_Developer.png" alt="Early Bot Developer">
            <img src="https://path_to_your_custom_badge/Early_Supporter.png" alt="Early Supporter">
            <img src="https://path_to_your_custom_badge/Active_Developer.png" alt="Active Developer">
            <img src="https://path_to_your_custom_badge/24_Month_Boost_Badge.png" alt="24 Month Boost Badge">
            <img src="https://path_to_your_custom_badge/Gold_Hype_Squad_Hunter.png" alt="Gold Hype Squad Hunter">
        </div>
    </div>

    <script>
        const userId = '1153976202600648714';
        const lanyardApiUrl = `https://api.lanyard.rest/v1/users/${userId}`;

        async function fetchData() {
            const response = await fetch(lanyardApiUrl);
            const data = await response.json();

            document.getElementById('avatar').src = `https://cdn.discordapp.com/avatars/${userId}/${data.data.discord_user.avatar}.png`;
            document.getElementById('username').innerText = `${data.data.discord_user.username}#${data.data.discord_user.discriminator}`;

            // Add Lanyard badges (you need to customize this part according to the API response)
            const badgesContainer = document.getElementById('badges');
            // Example of adding a badge based on Lanyard data
            // if (data.data.discord_user.public_flags & FLAG_CONSTANT) {
            //     const badge = document.createElement('img');
            //     badge.src = 'URL_TO_BADGE_IMAGE';
            //     badge.alt = 'Badge Description';
            //     badgesContainer.appendChild(badge);
            // }
        }

        fetchData();
    </script>
</body>
</html>

## Discord Profile

Check out my [Discord Profile](https://your_github_username.github.io/your_repository_name/discord_profile.html) to see my badges and more!
