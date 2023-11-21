# cctvcamera
cctv camera
import requests

def add_github_account(username, token):
    url = f"https://api.github.com/user/following/{username}"
    headers = {
        "Authorization": f"Bearer {token}",
        "Accept": "application/vnd.github.v3+json"
    }

    response = requests.put(url, headers=headers)

    if response.status_code == 204:
        print(f"Successfully added {username} to your GitHub following list!")
    elif response.status_code == 404:
        print(f"User {username} not found on GitHub.")
    elif response.status_code == 401:
        print("Unauthorized. Please check your GitHub personal access token.")
    else:
        print(f"Error: {response.status_code} - {response.text}")

# Replace 'your_username' with the GitHub username you want to follow
# Replace 'your_token' with your GitHub personal access token
add_github_account('your_username', 'your_token')
