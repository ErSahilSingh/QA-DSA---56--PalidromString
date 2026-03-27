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


//2nd approch for two pointer

  var isPalindrome = function(s) {
    s = s.toLowerCase();
    let i = 0;
    let j = s.length - 1;
    while (i < j) {
        if (!s[i].match(/[a-z0-9]/i)) {
            ++i;
        }
        else if (!s[j].match(/[a-z0-9]/i)) {
            --j;
        }
        else if (s[i] === s[j]) {
            ++i;
            --j;
        }
        else {
            return false;
        }
    }
    return true;
  };
      
