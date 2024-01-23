# ICP Website Screenshot 

This is an Internet Computer (ICP) project that provides a service to take screenshots of your favourite web pages.

## How it works

The project exposes an update method `get_screenshot` which takes a URL as input. It makes an HTTP request to the RapidAPI's website screenshot service with the provided URL and returns a screenshot.

The HTTP request is made using the `http_request` function from the `ic_cdk::api::management_canister::http_request` module. The request includes several headers, including the RapidAPI key and host.

## Deployment

To deploy this canister, follow these steps:

1. Install [IC SDK](https://internetcomputer.org/docs/current/developer-docs/setup/install/).
   
2. Clone this repository.
 ```bash
   git clone https://github.com/mervanerenci/icp_http_request.git
```
3. Navigate to the project directory.
   
4. Start a local Internet Computer replica by running:
```bash 
   dfx start --background
``` 

5. Replace `"YOUR-API-KEY-HERE"` in the `get_screenshot` method with your actual RapidAPI key before deploying.
   
6. Deploy the canister to the local replica. 
```bash
   dfx deploy
```

Note: For production, it is recommended to store API keys and other private values in a .env file instead of hardcoding in code

## Usage

To use the canister, you have 2 options. 
1. Use generated Candid UI to call the `get_screenshot` method.

2. Or you can call the `get_screenshot` method with a URL as input. For example, to take a screenshot of the DFINITY website, run the following command:

```bash
dfx canister call screenshot_service get_screenshot '("https://dfinity.org/")'
```



## Example


![icp_homework_http_candid](https://github.com/mervanerenci/icp_http_request/assets/101268022/78ced906-990e-4932-8556-b6d545746e5a)

![icp_homework_http_screenshot1](https://github.com/mervanerenci/icp_http_request/assets/101268022/c57dde78-6baa-4f5b-9e98-4d8423497b22)

![icp_homework_http_screenshot2](https://github.com/mervanerenci/icp_http_request/assets/101268022/e579abd3-1a82-4a50-b446-c31813a52017)





This project was created as part of the [Internet Computer Internship Bootcamp](https://www.risein.com/bootcamp-details/internet-computer-internship-bootcamp/) by Rise In.
