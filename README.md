const mockApiResponse = {
  data: [
    {
      name: 'Mixmax',
      budget_name: 'Software subscription',
      owner_id: 1,
      spent: {
        value: 100,
        currency: 'SGD'
      },
      available_to_spend: {
        value: 1000,
        currency: 'SGD'
      },
      card_type: 'burner',
      expiry: '9 Feb',
      limit: 100,
      status: 'active'
    },
    {
      name: 'Quickbooks',
      budget_name: 'Software subscription',
      owner_id: 2,
      spent: {
        value: 50,
        currency: 'SGD'
      },
      available_to_spend: {
        value: 250,
        currency: 'SGD'
      },
      card_type: 'subscription',
      limit: 10,
      status: 'active'
    }
  ],
  page: 1,
  per_page: 10,
  total: 100
};

// Example usage:
const cardData = mockApiResponse.data;

// Displaying the card data
cardData.forEach((card) => {
  console.log('Card Name:', card.name);
  console.log('Budget Name:', card.budget_name);
  console.log('Owner ID:', card.owner_id);
  console.log('Spent:', card.spent.value, card.spent.currency);
  console.log('Available to Spend:', card.available_to_spend.value, card.available_to_spend.currency);
  console.log('Card Type:', card.card_type);
  if (card.card_type === 'burner') {
    console.log('Expiry:', card.expiry);
    console.log('Limit:', card.limit);
  } else if (card.card_type === 'subscription') {
    console.log('Limit:', card.limit);
  }
  console.log('Status:', card.status);
  console.log('--------------------');
});
