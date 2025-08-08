# my-first-repo
just testing github
import requests

def get_btc_price():
    url = "https://api.coindesk.com/v1/bpi/currentprice/BTC.json"
    response = requests.get(url)
    if response.status_code == 200:
        data = response.json()
        price = data["bpi"]["USD"]["rate"]
        print(f"💰 Current Bitcoin Price: ${price}")
    else:
        print("❌ Failed to fetch data.")

if __name__ == "__main__":
    get_btc_price()
