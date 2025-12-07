# DW
Diseware
```
const dicewareWords = [
    'амфибрахий', 'анахорет', 'анчутка', 'афедрон', 'выхухоль', 'гомоморфизм', 'даздраперма',
    'драндулет', 'женонеистовый', 'жупел', 'капучинатор', 'козлодёр', 'кулебяка', 'многочлен',
    'мормышка', 'мужатица', 'мужатка', 'наопако', 'ококоветь', 'пердимонокль', 'пéточить',
    'пипидастр', 'пипин', 'поползновение', 'пюпитр', 'сопатка', 'странь', 'супря', 'сусеки',
    'тарталетка', 'форшмак', 'хухря', 'членистоногие', 'шмакодявка', 'шпингалет', 'шуфлядка',
    'нейрон', 'киборг', 'хакер', 'матрица', 'сингулярность', 'интерфейс', 'протокол',
    'шифр', 'алгоритм', 'бит', 'байт', 'квант', 'фотон', 'электрон', 'процессор'
];

function generateMemorablePassword() {
    let password = '';
    const wordCount = 4;
    
    for (let i = 0; i < wordCount; i++) {
        const randomIndex = Math.floor(Math.random() * dicewareWords.length);
        password += dicewareWords[randomIndex];
        if (i < wordCount - 1) password += '-';
    }
    
    const randomNumber = Math.floor(Math.random() * 90) + 10;
    const symbols = '!@#$%^&*';
    const randomSymbol = symbols[Math.floor(Math.random() * symbols.length)];
    
    password += randomNumber + randomSymbol;
    
    return password;
}
```
