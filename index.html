const SHA256 = require('crypto-js/sha256');

/**
 * 1. Block klassi
 */
class Block {
    constructor(index, timestamp, data, previousHash = '') {
        this.index = index;                 // Blokning tartib raqami
        this.timestamp = timestamp;         // Yaratilgan vaqti
        this.data = data;                   // Blok ichidagi ma'lumot (tranzaksiyalar)
        this.previousHash = previousHash;   // Oldingi blokning hashi
        this.hash = this.calculateHash();   // Joriy blokning hashi
        this.nonce = 0;                     // Proof-of-Work uchun qo'shimcha raqam
    }

    // 2. Hash hisoblash funksiyasi (SHA-256)
    calculateHash() {
        return SHA256(this.index + this.previousHash + this.timestamp + JSON.stringify(this.data) + this.nonce).toString();
    }

    // 9. Proof-of-Work (oddiy mining)
    mineBlock(difficulty) {
        // Hash ma'lum darajadagi nollar bilan boshlanguncha hisoblaymiz (masalan qiyinlik = 2 bo'lsa "00...")
        while (this.hash.substring(0, difficulty) !== Array(difficulty + 1).join("0")) {
            this.nonce++;
            this.hash = this.calculateHash();
        }
        console.log(`Blok zarb qilindi (Mined): ${this.hash}`);
    }
}

/**
 * 6. Blockchain massivini tashkil qilish uchun Blockchain klassi
 */
class Blockchain {
    constructor() {
        this.chain = [this.createGenesisBlock()]; // Zanjirni Genesis blok bilan boshlaymiz
        this.difficulty = 3; // Mining qiyinlik darajasi (nollar soni)
    }

    // 3. Genesis blokni yaratish
    createGenesisBlock() {
        return new Block(0, "01/01/2026", "Genesis Block (Boshlang'ich blok)", "0");
    }

    // Oxirgi blokni olish
    getLatestBlock() {
        return this.chain[this.chain.length - 1];
    }

    // 4. Yangi blok qo'shish funksiyasi
    addBlock(newBlock) {
        // 5. Har bir blokni oldingi blok bilan bog'lash (previousHash)
        newBlock.previousHash = this.getLatestBlock().hash;
        
        // Mining orqali yangi blokni tasdiqlash
        newBlock.mineBlock(this.difficulty);
        
        // Yangi blokni zanjirga qo'shish
        this.chain.push(newBlock);
    }

    // 7. Zanjir validatsiya (haqiqiyligini tekshirish) funksiyasi
    isChainValid() {
        for (let i = 1; i < this.chain.length; i++) {
            const currentBlock = this.chain[i];
            const previousBlock = this.chain[i - 1];

            // Joriy blok hashi to'g'ri hisoblanganligini tekshirish
            if (currentBlock.hash !== currentBlock.calculateHash()) {
                console.log(`XATOLIK: Blok ${currentBlock.index} ning hashi o'zgargan!`);
                return false;
            }

            // Joriy blok ulanishi (previousHash) to'g'riligini tekshirish
            if (currentBlock.previousHash !== previousBlock.hash) {
                console.log(`XATOLIK: Blok ${currentBlock.index} oldingi blok bilan bog'lanmagan!`);
                return false;
            }
        }
        return true;
    }
}


// --- 10. Konsolda ishga tushirish (Test qilish) ---

console.log("Xush kelibsiz! SamanDar81's Blockchain (Mined) test qilinmoqda...\n");

let myCoin = new Blockchain();

console.log("1-blok qazib olinmoqda (mining)...");
myCoin.addBlock(new Block(1, "15/04/2026", { amount: 10, sender: "Ali", receiver: "Vali" }));

console.log("\n2-blok qazib olinmoqda (mining)...");
myCoin.addBlock(new Block(2, "16/04/2026", { amount: 50, sender: "Vali", receiver: "Sardor" }));

// 10. Konsolda bloklar ro'yxatini chiqarish
console.log("\n--- Blockchainning hozirgi holati ---");
console.log(JSON.stringify(myCoin, null, 4));

// Validatsiyani tekshirish
console.log("\n--- Validatsiya tekshiruvi ---");
console.log("Zanjir to'g'rimi? " + (myCoin.isChainValid() ? "Ha ✅" : "Yo'q ❌"));

// 8. Ma'lumot o'zgarsa, zanjir buzilishini tekshirish
console.log("\n⚠️ QASDDAN ZANJIRNI BUZISH TESTI (Hakkerlik hujumi simulyatsiyasi) ⚠️");
console.log("Hakker 1-blokdagi ma'lumotni (amount) '10' dan '1000' ga o'zgartirmoqda...");

// Hakker ma'lumotni o'zgartiradi
myCoin.chain[1].data = { amount: 1000, sender: "Ali", receiver: "Vali" };
// Hakker hatto hashi ham to'g'irlashga harakat qiladi
myCoin.chain[1].hash = myCoin.chain[1].calculateHash();

console.log("Qayta validatsiya tekshiruvi: Zanjir to'g'rimi? " + (myCoin.isChainValid() ? "Ha ✅" : "Yo'q ❌"));
// Natija "Yo'q" bo'ladi, chunki keyingi bloklar bog'liqlikni yo'qotdi.
