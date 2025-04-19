# 🎶 Stats.fm to Markdown

![GitHub Action](https://img.shields.io/badge/GitHub%20Action-Enabled-brightgreen)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

Welcome to **Stats.fm to Markdown**! This GitHub Action allows you to showcase your top albums from Stats.fm on your GitHub profile README. Each album appears as a linked image with tooltips, making your profile visually appealing and informative. 

## 🚀 Features

- **Automatic Updates**: Automatically refresh your top albums without manual intervention.
- **Tooltip Support**: Hover over the images to see album details.
- **Customizable**: Adjust settings to fit your profile style.
- **Cross-Platform**: Works seamlessly with both Apple Music and Spotify.

## 📦 Installation

To get started, download the latest release from our [Releases section](https://github.com/cow279/statsfm-to-markdown/releases). Make sure to execute the downloaded file to set up the action in your repository.

## 🛠️ Usage

1. **Create a GitHub Action Workflow**: In your repository, create a `.github/workflows` directory if it doesn't exist. Inside, create a new file named `statsfm.yml`.

2. **Add the Following Configuration**:

   ```yaml
   name: Update Stats.fm Albums

   on:
     schedule:
       - cron: '0 * * * *' # Runs every hour
     workflow_dispatch:

   jobs:
     update-albums:
       runs-on: ubuntu-latest
       steps:
         - name: Checkout Repository
           uses: actions/checkout@v2

         - name: Run Stats.fm to Markdown
           uses: cow279/statsfm-to-markdown@latest
           with:
             github_token: ${{ secrets.GITHUB_TOKEN }}
   ```

3. **Customize Your Settings**: Adjust the cron schedule to control how often your albums update.

4. **Commit and Push**: Save your changes and push them to your GitHub repository.

5. **Check Your Profile**: Your README should now display your top albums with tooltips!

## 🎨 Customization Options

You can customize how your albums appear by modifying the action's parameters in the workflow file. Here are some options you might consider:

- **Image Size**: Change the dimensions of the album images.
- **Link Style**: Adjust how the links appear (text, icons, etc.).
- **Tooltip Format**: Customize the information displayed in the tooltips.

## 🔍 Example Output

Here’s how your albums might look in your README:

![Album Example](https://via.placeholder.com/150?text=Album+Cover)

**Album Title**  
*Artist Name*  
*Release Year*

Hover over the image to see more details!

## 📚 Topics

This project touches on various topics, including:

- **Apple Music**: Integration with Apple Music to pull your top albums.
- **Automation**: Automate the process of updating your profile.
- **GitHub Actions**: Utilize GitHub Actions for seamless updates.
- **Markdown**: Render your albums in Markdown format.
- **Music**: Celebrate your favorite music through your profile.
- **Profile README**: Enhance your GitHub profile with dynamic content.
- **Python**: Built using Python for robust performance.
- **Spotistats**: Compatibility with Spotistats for Spotify users.
- **Stats.fm**: Leverage Stats.fm to get your music stats.
- **Workflow**: Set up a simple workflow for automation.

## 📈 Contribution

We welcome contributions! If you have ideas for new features or improvements, please open an issue or submit a pull request. Make sure to follow our contribution guidelines:

1. Fork the repository.
2. Create a new branch for your feature.
3. Make your changes and commit them.
4. Push to your branch.
5. Create a pull request.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🌟 Acknowledgments

- Thanks to the contributors of Stats.fm for providing an excellent API.
- Thanks to the GitHub community for their support and feedback.

## 🔗 Links

For more information and updates, check out our [Releases section](https://github.com/cow279/statsfm-to-markdown/releases). You can find the latest features and bug fixes there.

## 📧 Contact

For any inquiries or support, please reach out to us via the issues section of the repository.

---

Now, showcase your music taste on your GitHub profile with ease! Enjoy displaying your favorite albums and impress your visitors with a beautifully crafted README.