# project-currency converter
This is my first project 
<br>
Auther:sadaqat hussain
<br>
project name=currency converter
# Define the fiat_currency_converter function
def fiat_currency_converter(amount, from_currency, to_currency):
    # Simple conversion rates (hypothetical and not real-world values)
    conversion_rates = {
        # Fiat Currency Conversion Rates
        ('pkr', 'usd'): 0.0036,   # 1 PKR = 0.0036 USD
        <br>
        ('usd', 'pkr'): 278.0,    # 1 USD = 278 PKR
        <br>
        ('eur', 'pkr'): 307.11,   # 1 EUR = 307.11 PKR
        <br>
        ('pkr', 'eur'): 0.0033,   # 1 PKR = 0.0033 EUR
        <br>
        ('aed', 'pkr'): 76.09,    # 1 AED = 76.09 PKR
        <br>
        ('pkr', 'aed'): 0.013,    # 1 PKR = 0.013 AED
        <br>
        ('gbp', 'pkr'): 358.50,   # 1 GBP = 358.50 PKR
        <br>
        ('pkr', 'gbp'): 0.0028,   # 1 PKR = 0.0028 GBP
        <br>
        ('inr', 'pkr'): 3.74,     # 1 INR = 3.74 PKR
        <br>
        ('pkr', 'inr'): 0.27,     # 1 PKR = 0.27 INR
        <br>
        ('cad', 'pkr'): 208.67,   # 1 CAD = 208.67 PKR
        <br>
        ('pkr', 'cad'): 0.0048,   # 1 PKR = 0.0048 CAD
        <br>
        ('aud', 'pkr'): 182.34,   # 1 AUD = 182.34 PKR
        <br>
        ('pkr', 'aud'): 0.0055,   # 1 PKR = 0.0055 AUD
        <br>
        ('pkr','pkr'):1.00,#  1 pkr=0.00 pkr 
        <br>
    }
    
    # Check if the currency pair exists
    if (from_currency, to_currency) in conversion_rates:
        return amount * conversion_rates[(from_currency, to_currency)]
    else:
        return "Conversion rate not available."

# Define the crypto_currency_converter function
def crypto_currency_converter(amount, from_currency, to_currency):
    # Simple conversion rates (hypothetical and not real-world values)
    conversion_rates = {
        # Cryptocurrency Conversion Rates
        ('pkr', 'eth'): 0.0000014,  # 1 PKR = 0.0000014 ETH
        <br>
        ('eth', 'pkr'): 73203.19,   # 1 ETH = 73,203.19 PKR
        <br>
        ('pkr', 'btc'): 0.00000003, # 1 PKR = 0.00000003 BTC
        <br>
        ('btc', 'pkr'): 16331063.65,# 1 BTC = 16,331,063.65 PKR
        <br>
        ('pkr', 'ltc'): 0.000014,   # 1 PKR = 0.000014 LTC
        <br>
        ('ltc', 'pkr'): 7321.0,     # 1 LTC = 7321 PKR
        <br>
        ('pkr', 'doge'): 0.05,      # 1 PKR = 0.05 DOGE
        <br>
        ('doge', 'pkr'): 20.0,      # 1 DOGE = 20 PKR
        <br>
        ('pkr', 'bnb'): 0.0000012,  # 1 PKR = 0.0000012 BNB
        <br>
        ('bnb', 'pkr'): 82141.0,    # 1 BNB = 82,141 PKR
        <br>
        ('pkr', 'xrp'): 0.02,       # 1 PKR = 0.02 XRP
        <br>
        ('xrp', 'pkr'): 49.0,       # 1 XRP = 49 PKR
        <br>
    }
    
    # Check if the currency pair exists
    if (from_currency, to_currency) in conversion_rates:
        return amount * conversion_rates[(from_currency, to_currency)]
    else:
        return "Conversion rate not available."

# Main Program Logic
print("Enter the currency type you want to change")
print("1 = Fiat Currency")
print("2 = Cryptocurrency")

choice = int(input())

amount = float(input("Now type the amount that you want to change: "))

if choice == 1:
    from_currency = input("Now type which fiat currency you want to change (e.g., pkr, usd, eur): ").lower()
    to_currency = input("Now type the currency you want to change to (e.g., usd, pkr, eur): ").lower()
    result = fiat_currency_converter(amount, from_currency, to_currency)

elif choice == 2:
    from_currency = input("Now type which cryptocurrency you want to change (e.g., btc, eth, doge): ").lower()
    to_currency = input("Now type the cryptocurrency you want to change to (e.g., eth, btc, pkr): ").lower()
    result = crypto_currency_converter(amount, from_currency, to_currency)

else:
    result = "Invalid selection. Please choose either 1 or 2."

print(result)
