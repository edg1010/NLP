// membuat function dengan input e
checkPhoneNumber = (e) => {
    var regex = /^[+]6[025][0-9]+$/;
    // ^        ==> berarti mencocokan dari awal
    // [+]      ==> karakter pertama harus berupa tanda +
    // 6        ==> karakter kedua harus berupa angka 6
    // [025]    ==> karakter ketiga harus berupa 0, 2, atau 5
    // [0-9]+   ==> semua karakter setelah karakter ke-3 harus berupa angka
    // $        ==> mencocokan string sampai karakter terakhir
    // menbandingkan regex dengan input
    if (e.match(regex)) {
        console.log(e + " | Valid"); // jika cocok
    } else {
        console.log(e + " | Invalid"); // jika tidak cocok
    }
};
console.log("");
console.log("Phone Number | Status");
console.log("----------------------");
checkPhoneNumber("+62215262578");   // valid
checkPhoneNumber("+60358577");      // valid
checkPhoneNumber("+60388888000");   // valid
checkPhoneNumber("+62215262578a");  // invalid karena karakter terakhir bukan angka
checkPhoneNumber("+62215a262578");  // invalid karena ada karakter ditengah yang bukan angka
checkPhoneNumber("a+62215262578");  // invalid karena awalan bukan tanda +
checkPhoneNumber("62215262578");    // invalid karena tidak diawali dengan +
checkPhoneNumber("+61215262578");   // invalid karena karakter ketiga bukan 0, 2, atau 5
console.log("----------------------");

checkEmailAddress = (e) => {
    var regex = /^[a-zA-Z0-9.]+@[a-zA-Z0-9]+[.]((edu)([.][a-zA-Z]{2})?|(ac)([.][a-zA-Z]{2}))$/;
    // ^                        ==> berarti mencocokan dari awal
    // [a-zA-Z0-9.]+            ==> string diawal harus berupa huruf, angka, dan . saja
    // @                        ==> setelah string, karakter harus @
    // [a-zA-Z0-9]+             ==> setelah karakter @, string harus berupa alphanumberic
    // [.]                      ==> setelah string, karakter harus .
    // (edu)                    ==> string harus edu
    // ([.][a-zA-Z]{2})?        ==> string harus berupa . diikuti oleh 2 karakter berupa huruf
    //                              tanda ? berarti string tersebut boleh ada atau tidak
    //                              hanya bisa 2 huruf karena kode negara hanya terdiri dari 2 huruf
    // (edu)([.][a-zA-Z]{2})?   ==> berarti string dapat berupa edu atau
    //                              edu.id (id dapat diubah menjadi 2 huruf apa saja)
    // (ac)                     ==> string harus ac
    // ([.][a-zA-Z]{2})         ==> string harus berupa . diikuti oleh 2 karakter berupa huruf
    //                              hanya bisa 2 huruf karena kode negara hanya terdiri dari 2 huruf
    // (ac)([.][a-zA-Z]{2})     ==> berarti string harus berupa ac.id (id dapat diubah menjadi
    //                              2 huruf apa saja)
    // ((edu)([.][a-zA-Z]{2})?|(ac)([.][a-zA-Z]{2}))    ==> string diakhir bisa berupa
    //                                                      edu, edu.id, atau ac.id
    //                                                      (id dapat diubah menjadi 2 huruf
    //                                                      apa saja)
    // $                        ==> mencocokan string sampai karakter terakhir
    if (e.match(regex)) {
        console.log(e + " | Valid");
    } else {
        console.log(e + " | Invalid");
    }
};
console.log("Email Address | Status");
console.log("----------------------");
checkEmailAddress("jolly.wanda@bee.ac.id"); // valid
checkEmailAddress("jojo@bee.ac.uk");        // valid
checkEmailAddress("jolly.wanda@bee.edu");   // valid
checkEmailAddress("jojo@bee.edu.au");       // valid
checkEmailAddress("edgar@binus.ac");        // invalid karena ac harus diikuti oleh .id
checkEmailAddress("edgar@binus.4c.id");     // invalid invalid karena penulisan 4c harus berupa edu atau ac
checkEmailAddress("edgar@binus.ac.1d");     // invalid karena penulisan 2 karakter terakhir hanya boleh terdiri dari huruf
checkEmailAddress("edgar@b1nus.edu");       // invalid karena string setelah @ hanya boleh terdiri dari huruf
checkEmailAddress("edgar_001@binus.ac.id"); // invalid karena string diawal hanya bisa berupa aplhanumerik dan . saja
checkEmailAddress("edgar@binus.ac.idn");    // invalid karena string terakhir hanya boleh terdiri dari 2 huruf saja
console.log("----------------------");
