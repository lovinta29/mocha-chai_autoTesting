# mocha-chai_autoTesting

Require:
- Node.js
- Code Editor (e.g. Visual Studio Code)

Assertion
Assertion digunakan untuk mendefinisikan output yang diharapkan (expectation result) dari suatu fungsi atau program.

Assertion Library: Chai JS (https://www.chaijs.com/)
- Chai                          : BDD/TDD assertion library untuk Node.js
- Chai instalasi                : npm install chai
- Chai set-up                   : pada package.json tambahkan "type": "module" untuk menggunakan Ecmascript Modules agar sintaks import dan export dapat digunakan.
- Chai type                     : expect, assert, should
- Chai importing example        :
  const expect = require('chai').expect;
  expect('x').to.equal('x') 
                -> to dari BDD (Behavior Driven Development): bahasa yang sederhana sehingga orang tanpa pengetahuan teknis juga bisa memahami apa yang sedang terjadi.
                -> BDD berkaitan dengan Gerkhin (Given, When, And & Then)
- Chai Language Chains (BDD)    : to, be, been, is, that, which, and, has, have, with, at, of, same, but, does, still, also
- Chai Frequently Used Methods (https://www.chaijs.com/api/bdd/): 
  1. .equal()   : expected value strictly equal '===' dengan actual value; 
  2. .a()       : expected tipe data equal dengan tipe data actual value;
  3. .include() : expected value include atau ada dalam bagian dari actual value;
  4. .empty     : expected value kosong;
  .deep      : expected value deep equality atau dimiliki oleh actual value;
               -> penggunaan: to.deep.include()
  5. .length()  : expected value length atau panjangnya equal dengan actual value;


Testing Framework JavaScript: Mocha JS (https://mochajs.org/)
- Mocha             : framework pengujian JavaScript yang berjalan di Node.js dan browser, sehingga pengujian dapat dilakukan secara asynchronus.
- Mocha instalasi   : npm install mocha
- Mocha set-up      : pada package.json bagian scripts, tambahkan "test": "mocha [namaFileTest.js]" untuk menjalankan pengujian secara otomatis. 
                                                            -> mocha **/*.test.js : artinya menjalankan semua file dengan nama dan/atau akhiran test.js di seluruh folder dalam project.
- Mocha running     : npm run test atau npm test
- Mocha - Test file :
  - Test file berekstensi .test.js
  - Dalam .test.js digunakan:
    1. Fungsi describe() dari Mocha untuk mendefinisikan test suite (fitur yang diuji; kumpulan test case).
                        -> describe() dapat bersarang (nested) di describe() lainnya, misalnya untuk medefenisikan test scenario di dalamnya.
    2. Fungsi it() dari Mocha untuk mendefinisikan test case (langkah spesifik pengujian).

- Mocha Hook        : digunakan dalam fungsi describe()
  1. before()    : fungsi yang akan dijalankan sebelum pengujian (per block atau describe() function) dimulai;
  2. after()     : fungsi yang akan dijalankan setelah pengujian (describe() function) selesai;
  3. beforeEach(): fungsi yang akan dijalankan sebelum setiap test case (per it() function) dijalankan;
  4. afterEach() : fungsi yang akan dijalankan setelah setiap test case (it() function) selesai
  
- Mocha-Manually Controlling/Debugging Test
 1. .skip(): mengabaikan/melewati pengujian (test case) tertentu;
 2. .only(): menjalankan pengujian (test case) tertentu saja (abaikan pengujian lainnya);
