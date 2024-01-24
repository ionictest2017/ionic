# ionic




async postAddressTextQuery(prompt: string) {
        
  await fetch(
    this.apiUrl2,
      {
      body: JSON.stringify(
        {
          "textQuery" : "Spicy Vegetarian Food in Sydney, Australia"
        },
        
      
      ),
      method: "POST",
      headers: {
          "content-type": "application/json",
          "X-Goog-Api-Key": this.apiKey,
          "X-Goog-FieldMask":"places.displayName,places.formattedAddress,places.priceLevel"
      },
          }
  ).then((res) => {
  console.log(res)
  })
}
