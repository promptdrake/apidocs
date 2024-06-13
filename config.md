---
outline: deep
---

# Config Telegram bot
**.json**
```json
{
    "bot_token": " ", // buat di https://t.me/botfather
    "owner_chatid": " ", // cek di https://t.me/getmy_idbot
    "store_name": " ", // nama storemu

/*
@* Buat grub private
@* Masukin bot https://t.me/GetMyChatID_Bot sama bot checkout mu
@* Lalu ketik /id dan copy chat_idnya
*/
    "invoice_logger": " ",


    "owner_usn": " ", //usernamemu
    "stok_chatid":" ", // sama kek invoice_logger


    "trakteer_depo": " ", // (Abaikan) gunakan jika kamu menggunakan trakteer.id gateway Misal https://trakteer.id/aisbirkun

    "enable_custom_scripting": true, // Custom script case.js
    "port_webhook": "25569", // (Abaikan) Port Buat nerima notif trakteer.id
    "endpoint_callback_trakteer": "secretrareepic", // (Abaikan) endpoint buat nerima trakteer.id

// Pilih salah satu
    "deposit_settings": { 
        "only_admin_deposit": false,
        "enabled_trakteer_deposit": false,
        "paymentgateway": true
    },

// Pilih salah satu jika menggunakan payment gateway
    "payment_type":{
        "midtrans": false,
        "paydisini": true
    },

    /*
    Setting Fee paydisini
    1= ke customer
    2= ke merchant (Owner bot)
    */
    "paydisini_conf": {
        "fee": 1
    },

    "enable_refferal_link": false, // link refferal

/*
Hadiah link refferal
*/
    "ref_conf" : {
        "invite": 100,
        "join": 50
    },

    "enable_question_on_start": true, //  nanya pertanyaan tiap user ketik /start

    /* Kalok dimatiin default identitasnya dibawah ini */
    "default_user_if_false": {
        "username": "Anonymous",
        "birthday": "01-01-2000"
    },

    /*
    Stiker tiap ketik /start
    */
    "stiker_start_fileid":"CAACAgUAAxkBAAECPLdl9VzgQCKvb0Q73DIiU6qkZ3NtJAACNQoAAq4wYFaIM0H-IASMdTQE",

    /*
    Button
    */
    "button_menu": {
        "informasi": "🪪 Information",
        "deposit": "💳 Deposit",
        "list": "🛍️ List Produk",
        "stock": "🛒 Stock"
    }
}
```

**.ENV**
```dart
AISBIR_USERNAME= " " // USername apikey yang diberikan aisbir
AISBIR_KEY= " " // apikey yang diberikan aisbir

// Jika kamu menggunakan midtrans
MIDTRANS_SERVER_KEY= "" // server key midtransmu

/*
sandbox: Ujicoba
production: Langsung masuk ke midtrans
*/
MIDTRANS_MODE= "sandbox" 
MIDTRANS_PAYMENT_EXPIRY= "5" // payment expired midtrans (Dalam Menit)
MIDTRANS_AUTOCHECK_THRESSHOLD= "5000" // Auto cek Midtrans (Dalam Milisecond)

// Jika kamu menggunakan paydisini
PAYDISINI_KEY=" " // pergi ke settings copy api token

PAYDISINI_FEE="1"  
/*
# 1 = customer
# 2 = merchant
*/



ENABLE_BTN_PAYGATEWAY="true" // Cek payment make button cek payment
ENABLE_AUTOUPDATE="true" // enable auto update

ENABLE_NOTIFICATION_STOCK="false" // Ingfo kalok ada stok terbaru update

/*
Ini digunakan ketika orang pengen claim giveaway
dia perlu beli setidaknya 1 produk dulu atau engga
biar ga ngeclaim geratisan
*/
REQUIRE_VERIFICATION="false" // true / false

// abaikan
NGROK_AUTH_TOKEN="2741VaC5nJPY1Z6SymMUFjUvAAn_4d3v3bo8B5aFKkkox79dW"
NGROK_PORT="3000"

/* Auto Backup By asbir */
ENABLE_AUTOBACKUP="false"
DISCORD_HOOK=""
```