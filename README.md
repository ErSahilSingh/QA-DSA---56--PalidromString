# QA-DSA---56--PalidromString

/**
 * @param {string} s
 * @return {boolean}
 */
var isPalindrome = function(s) {
    s=s.toLowerCase()
    let filterString=""
    let rev=""
    for(let i=0;i<s.length;i++){
        if(s[i].match(/[a-z0-9]/i)){
            filterString=filterString+s[i];
            rev=s[i]+rev;
        }
    }
    return filterString===rev
};
