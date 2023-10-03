<template>
    <div>
       VOLUME {{ convertToRoman(viewCount) }}
    </div>
</template>
  
<script>
import Cookies from 'js-cookie';

export default {
    data() {
        return {
            viewCount: 0
        };
    },
    mounted() {
        if (!Cookies.get('viewCount')) {
            this.viewCount = 1;
            Cookies.set('viewCount', this.viewCount);
        } else {
            this.viewCount = parseInt(Cookies.get('viewCount')) + 1;
            Cookies.set('viewCount', this.viewCount);
        }
    },
    methods: {
        convertToRoman(num) {
            const romanNumerals = [
                ["", "I", "II", "III", "IV", "V", "VI", "VII", "VIII", "IX"],
                ["", "X", "XX", "XXX", "XL", "L", "LX", "LXX", "LXXX", "XC"],
                ["", "C", "CC", "CCC", "CD", "D", "DC", "DCC", "DCCC", "CM"],
                ["", "M", "MM", "MMM"]
            ];

            let roman = "";
            let digits = 0;

            while (num > 0) {
                const digit = num % 10;
                roman = romanNumerals[digits][digit] + roman;
                num = Math.floor(num / 10);
                digits++;
            }

            return roman;
        },
    },
}
</script>