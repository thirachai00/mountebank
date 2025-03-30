# install Mountebank
npm install -g mountebank

# run test Mountebank
mb
# check install -> localhost:2525

# install extention EJS
# run : use command 
    # mb --configfile imposters.ejs --allowInjection

# CURL Success
curl --location 'http://localhost:6969/customer/v1/profiles/create' \
--header 'Content-Type: application/json' \
--data '{
    "requestTransactionId":"xxx",
    "name":"Name xxx",
    "lastname":"Last name xxx",
    "cardIdentification":"XY12121212121"
}'

# CURL Error
curl --location 'http://localhost:6969/customer/v1/profiles/create' \
--header 'Content-Type: application/json' \
--data '{
    "requestTransactionId":"xxx",
    "name":"Name xxx",
    "lastname":"Last name xxx",
    "cardIdentification":"FF12121212121"
}'