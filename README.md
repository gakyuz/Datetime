# Datetime

Datetime.js is a minimalist JavaScript library that parses, validates, manipulates, and displays dates and times for modern browsers with comfortable modern API.

* 🕒 Quick and accurate
* 🔥 Chainable
* 🌐 I18n support
* 📦 3kb mini library
* 👫 All browsers supported

## Getting started

### Documentation

You can find for more details, API, and other docs on [DOCUMENTATION](DOCUMENTATION.md).

### Installation

```console
npm install @olton/datetime --save
```

### API

It's easy to use Datetime APIs to parse, validate, manipulate, and display dates and times.

#### Parse
```javascript
datetime();
datetime("2020");
datetime("2020-12-31");
datetime("2020-12-31 23:59");
datetime(2020, 12, 31, 23, 59);
datetime([2020, 12, 31, 23, 59]);
Datetime.parse(...);
Datetime.fromString("16 November 1961 15:24", "dd mm %y h:i", "en")
Datetime.fromString("16 Ноября 1961 15:24", "dd mm %y h:i", "ru")
```

#### Display
```javascript
datetime().format('{YYYY} MM-DDTHH:mm:ss sss Z A');
datetime().strftime('{%Y} %n-%dT%H:%M:%S %Q %z %p');
```

#### Get & set
```javascript
datetime().set('month', 3).month();
datetime().month(3).month();
```

#### Manipulate
```javascript
datetime().add(3, 'day').add(1, 'hour');
datetime().addDay(3).addHour(1);
```

#### Align (Start From)
```javascript
datetime().align("year"); // Will alignment to 1st Jan of year
datetime().align("month"); // Will alignment to 1st day of month
```

#### Compare
```javascript
datetime("2020").older("2021"); // return true
datetime("2020").younger("1972"); // return true
datetime("2020").between("2019", "2021"); // return true
datetime("2020-21-12").diff("1972-21-12"); // return {day: 17532, hour: 420768, millisecond: 1514764800000, minute: 25246080, month: 576, second: 1514764800, year: 48}
datetime("2020-21-12").distance("1972-21-12", "year"); // return 48
```

#### Information
```javascript

```