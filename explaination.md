** Fun with CSS3 - Pivotal Labs Logo

After spending a lot of time doing Go programming for Cloud Foundry and lots of 
infrastructure configuration for a vmware product suite, I have the need for something
purely aesthetic. It started with a placeholder for my github page dbellotti.github.io 
but when one of my coworkers took an interest and put up my 'art' on one of the monitors 
that was being used to display the chillestmonkey.com. This made me start to think about
some other cool pieces of art I could produce for the office monitors and naturally I 
decided to attempt to recreate the Labs logo using only CSS3 with an additional plan of
talking about what it took in a 3 minute lightning talk that would be held the following
week.

So here we go...

1. First boilerplate html and css with the first elements of the logo
```
<head>
  <link type="text/css" href="style.css" rel="stylesheet">
</head>

<body class="white-noise-bkg">
  <div class="container centered point-of-view">
    <div class="pivotal">
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="white-sphere"></div>
      <div class="red-sphere"></div>
    </div>
  </div>
</body>
```
index.html

Add some flare...
```
.white-noise-bkg {
    background-color: rgba(0, 119, 110, 0.5);
}

.bar {
    display: block;
    height: 100px;
    width: 1000px;
    margin: 10px;
    border-radius: 10px;
}

.bar:nth-child(1) { background-color: rgba(0, 118, 196, 0.9); }
.bar:nth-child(2) { background-color: rgba(122, 169, 221, 0.9); }
.bar:nth-child(3) { background-color: rgba(199, 216, 242, 0.9); }

.white-sphere {
    display: block;
    height: 100px;
    width: 100px;
    background-color: rgba(255, 255, 255, 0.9);
    margin: 10px;
    border-radius: 50px;
}

.red-sphere {
    display: block;
    height: 70px;
    width: 70px;
    background-color: rgba(199, 11, 43, 0.9);
    margin: 10px;
    border-radius: 35px;
}
```

2. Great, we have shapes all ready to go, lets add them together so they are
stacked in 3d space. 