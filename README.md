# **Chrome Dinosaur Game**

This is a replica of the Google Chrome Dinosaur Game.

I got most of the code from the real Chrome Dino Game (it _is_ open-source, after all).

## __Source Code__

```html
<!DOCTYPE html>
<html i18n-values="dir:textdirection;lang:language" dir="ltr" lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
    <style>
      /* Copyright 2014 The Chromium Authors. All rights reserved.
   Use of this source code is governed by a BSD-style license that can be
   found in the LICENSE file. */

      a {
        color: #585858;
      }

      .bad-clock .icon {
        background-image: -webkit-image-set(
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABICAMAAABiM0N1AAACBFBMVEUAAAD/U1P/VVX/UlL/U1P/U1P/U1P/UlL/U1P/////VVX/UlL/YGD/UlL/UlL/U1P/VFT/U1P/U1P/VVX/VVX/U1P/YmL/UlL/U1P/U1P/VFT/U1P/U1P/UlLxTU36T0/tS0vvTEzwS0vtS0vvTk7vTEz/Tk7vTk7wTEz/UFDyTEzuTU3wTU33VVXwTU3yTk7yTk7vTEz/UlLVRETrS0vsS0vtS0viSEjdRkbqSkrcRkbYRUXQQkLDPj7vTEzPQkK/PDzHQEDAPT3MQUHNQUG8PDzBPT29PDzWRETlSUnaRUW5OzvoSkruTEzfR0fnSUnRQkLeRkbpSkrgR0fTQ0PbRkbSQ0POQUHLQEDkSEjjSEj5T0/KQEDCPT3HPz/XRUW4Ojq7OzvXRETFPz/GPz+/PT3UQ0PZRUX4T0/3T0++PDzmSUnCPj7IPz/FPj7JQEDwTEy8OzvNQkK3OjrOQkLqk5PEPj65OjrLQUHIQEDyTU32Tk7y8PD2ZmbhR0faRkb0hobJPz/ogoLQenrMQEDKQUHSQkLdf3/kSUnrg4PnYWHUe3vafn7PQUHeR0f1Tk7zTU3ZfX3uhITzhobURETxTU24OzvAPDzvhITyhYX0Tk7gf3/WfX3RQ0PwhITnSkrqS0vigYHz8/PVQ0PkgYHmgYHlgYHSe3u6OzvxhYXthIT6UFDXDlesAAAAMnRSTlMA+QPfflOl7MsBFf4QO+ligO6NMx7EDXPV0mHqjrGO/tKNM9Vz7g2A6hBhxOke+TtisXITrPEAAAOwSURBVHhe7dhldxs5FAbgTkyJ06QOOlCmZdKgmZkpzMxYZmZaZGb4k5XHe2Y99ljXqdN+6vsDnnN1pdFI2vMy8zqvo9eotfUqHUXpVPVatUb/Ykpba3cjkqWxu7Vtp0qnsQsppsvYuQNmr6EFVUyLYW+VTENPLyKmt6ehGqe9A4HpaIedpmZURZqbIGcfhaoKtY/I1O1HVWd/HcE5gHaQA5UleT1wTRX7owz8gmNSlCr0qYmqDE0oSpTi3LU3IwJ0llFcBQrrqaEDEaDtyCaruDLL13gPIkETkcklRamn7DvtReSKJgNfcgpQb+kXbEBQRT6nP6YgGeROZwsZ2p6YDDjdM/ZyqEW+PxkRAOGK3Lbp1Y1yySiDuiBoYnPJvzJz3fN5GdQl258RAns06z8zturpL5eK9/FWCNr+KzA7uuYa6O+3lkmtRVB3FZB7dMY10u+wWi+UQN3/O/pGCIr4An7b9Plb2EnOlUiNegnSIAj6wrfkto2te08lk33Z7DO5pJEgNQhFArO2tbHbXit25uigXFJLkBaEcK9X1s6f81qzOHTQ8k0xpJWgehhyjp5xjZx7/D2uhw5OBeeLpXoJUoFQwOm3zQx4HH19c8HglGU+nCuSVBKkAyGf0za9PrKV7KNpesqSh4SnEqSTIAqEbrpXplc9W8ksna8HO+ZcSpKoHUCX/rS51j2O7Gd4YPOWcO6qIMSFizIIHtr9S3npoWvA68jS/9UjCKl4JvOfpKuy2egfUfpuwJvMBi3jknPlCl+QVLLph6WPTyV/HbeEw7lcDjvxOM/zg4vy6dciIJ+I0qM7wXHsmM2pVPwJrmdoMBRalC1INYLylSjdpS3hebNgzvdHdO4tJxaKPxENqlL69iquR0ilMhmeH+JDoeVENL2ANLJtBMoPovRzTqxHhLCzHI2a0of0so0NzN+i9Fu+z4VxhUIJ7JiYw0pbLSz9Ec/EeewM4nEl0lETwx4p2fzhfC1Kv+fr4UOikzaZWO5o6e8IzqcFqVBPSBwXyx4j/CAB6cbgkDhf6TR2uOMKv2w410TpwTJ2omkTw3DsiZOEQwQgnRbrwQ7LcbE3CMcaQDot1hPFDsPF3nyLcNAi5zJeP4kfcZ9/4mIx+9uEox+URXHeGQaPy/5OA+EwCmYBz7uJZbHz7nvA8RiS8uuHjdnf/wA4sIMZZhjcH/uHtV8hhjnsHNyNS82wfeOjul25Zv17sO7lXvxqv4rWfjmu/bpe+wPCK3zSgB9ZXs2zz3OaHfywRGWQFAAAAABJRU5ErkJggg==)
            1x,
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJAAAACQCAMAAADQmBKKAAACvlBMVEUAAAD/gID/gID/VVX/VVX/Tk7/YmL/YGD/VVXzUVH/XV32UlL/W1v2T0//WFj3UlL/UlL3UFD/WFjwTk7/U1P/U1PxTU3/V1fyT0//VFTzTk7/UlLwTU3/VVX0UFD/VFT/VFT1Tk7/VVX/VFT/U1PyT0//VFT/U1PxTEz/UlLuS0v/U1P/UlL/VFT0T0//U1P0Tk7/VFT/U1PuTU3/UlLzTU3/U1P/U1PwTEz/UlL/U1PvTU3/U1P/U1PxTU3/U1PzTk70Tk7/U1PyTk7/U1PzTk7/U1P/U1P6UFD/UlLzTk7/U1P/U1PyTk7/U1PtTEz/UlLyTU3/U1P/UlL/UlLxTk7/UlLvTEz/U1PvTU3/U1P/U1P/UlLxTEzxTU3zTU3/UlK7Ozu8Ozu8PDy9PDy+PDy+PT2/PDy/PT3APDzAPT3BPT3BPj7CPT3CPj7DPT3DPj7EPj7EPz/FPj7FPz/GPj7GPz/HPz/HQEDIPz/IQEDJPz/JQEDKQEDKQUHLQEDLQUHMQEDMQUHNQUHNQkLOQUHOQkLOZWXPQUHPQkLPZWXQQkLRQkLRQ0PSQkLSQ0PSZmbTQ0PTZmbUQ0PURETVQ0PVRETVaGjWRETWRUXXRETXRUXXaGjYRUXZRUXZaGjaRUXaRkbaaWnbRUXbRkbbaWncRkbdRkbdaWneRkbeR0ffRkbfR0ffa2vgR0fga2vhR0fhSEjha2viR0fiSEjia2vjSEjjbGzkSEjkSUnkbGzlSEjlSUnlbGzmSUnmbGznSUnnSkroSkrobW3pSkrqSkrqS0vqi4vrS0vriYnri4vsS0vsiYntS0vtTEzuTEzvTEzwTEzwTU3w6OjxTU3x6OjyTU3y6Ojy6eny8vLz8/P0Tk71Tk72Tk72cnL3T0/3cnL4T0/4cnL5T0/5c3P6T0/7UFD8UFD9UFD/UlJJWZWgAAAAYXRSTlMAAgQGDA0NEBUWFhwcHR0fHyAgNDQ3ODg9PT4+QkJDQ0lLS15fdHR1fHyEhIWGiIiJiYuVlaioqaurrK+vuLm5u7u7wsLExMXGxszM0tTU2dna2t/p7Ozt7fPz+fv+/v7+jD+tjQAAChVJREFUeNrtnP9/U1cZxwtsw81Z51ydE3E4EKxQkYqrIFjFCnbgZIAVATXSdukSWhMakrYkpCQUiWkbY7oaUlNbjYmdMXYaa6ZZLVmLcTEk2bIycHMiunL+C59zT9K0zZd7b+65W37o83vyer8+z+c5z3POveeWlS3HcizHcizHcizHciwH/1hdsX5Lze59Bw43HD/ecPjAvt01W9ZXrH53WO5aV113BOWMI3XV6+56R2FWrd1cfwIVjBP1m9eueodwHt5+FHGKo9sfFp/mwcqDiEccrHxQVJyHdkkQz5Dsekg0nEdqUVFR+4goOI/WoaKj7lHqOPfvQIJix/1UcVZuPIYExrGNK+nxrHkSUYgn19CSZ6sEUQnJVioile9F1GIvBSc91oAoRsNjAnFWbJMgqiHZtkJQF30cUY/HBfTce/YgEWLPPcXy3LcfiRL731MczwOHkEhx6IGi9BGNB4juK8I/+5GIsZ+3j1btQaLGHp61toJXvd9MxS0+1c9vPdqGigFS8SHaxqtfSIoC+j4fIgmPLlLOs3/NA51U3+bR18o5zxt8+3sGqLGLB9FertPIVlQsUGNjk5YH0VaO86EEFa9QU7P+f9xtxGmGXMl/Xl0A1Nws1b/NfarlkrRNCAlSSCrjQbSJw37nmBCgJgwku8CZ6Bj7TLsTCVZIJjdxJtrJuj9FAoBOMh6SyVp/0M+ZiG1PW4eEKyRvVaqsc1x32SznCUgYUFOTVCpTAJB6kCtR4ZOIWiRYoWdkbQq1Wt1p50hUW/D8BwkDamyUNj/T1qZsB6CzQxyJCp0f7RIM1CyXn2pTaNSaTl33MDeiXQXO6yRIqIdkUnmbQnlGrdF2dxt/yYlIkv/UrxIJAzp5sqlFKlcolWe6tFq9wdjjvsPl55V5gQ4JBWpqaWltBQud6ejS6Q09PSYPF6KDec97kWCFnm6RKxRKjaZDp9Mbe7gS5Ts93i4UqOlpWKVbFer2jo6u83rAMZvNv+FAtD3PzueoYKAmDKRSgqW1uvNGk8lkNvX62ImO5t4TrUWCgbCFWk9rOjtxxi4Cj7m31zzOTrQ2J9Bm4UDN0MdOn4ZFqEtnNF40Y55ei+UPrESbcwLVCweSycHTpzUaLSh0EYB6LcBjsbES1ed83nRCMFCzDPqYQq3RnNV2G8BCkC+Ltc9ms0ywEJ3I9TRrHRIMJJW2KRXQ6c+e7e7uAUuDPlYI26BtkoVoXQ6gauFAMukppVKt0mjPnes29pghWwBks9gGB+1/KfwP1bRGsyUpO6VQtCtxzZ8zXrrUZzZjHhvwDNodV3iPaUcoKCQDoHa1Fhxk6Llk7rNarBbMM2C32x2hQv9wJMfzXCQcqAUavbKjq0unMxou9fVhGqKP3WF3OqcL/UX2k+MKCkAgkFKthsZqgE5v7rOk8jVgdzgcTufQ1QJ/UZEFtIECkFyuVKk6YPKA0QMsbSN+Bn0cdodzeHgknP8v1mcBVVEAalUoVCq1Vq8zQNvoxUS2tDzDAFSIqCoLqIaGQiCQRtOl18MyzfAw/hkkRCMjrhFXJN9f1FDabyxRqBWAoG0YLlyAtgEL4gD2M8YBfZwjLteo+xrnvUc9BSBFu0rVqdEaQCBTf/+AlfjH4RzCOCOuUZfb7Y5x7WYHaACBhTo7u2EVgjZmtaby5WTyBfoAjsflyU10IAvoMAWgtnYVzELQVy/C3DEwgJcfh9PO2JkAeTxjY554rr84nAXUQAHohzAranR4FTKBQMz6nPGPa9TjcQOQ1/tKrhPQLKDjFIBe/VGHGjxtNJr6zJaBAazPvDyjRB/g8fpyEB2nCfTWzQxRl05rNBpM0Fah5pl8gZ2HiX8AyDPmfc7n8yY5AAlI2a2bGaIfw37MaOqx9NkgY86UQMDjAh430cfnGx+fZU+ZEFP/69UFROf1RhAI5sRBJwM0MjwC+mBHjzEZ83nHx/3+WVZTCyn7RUQ/McI03Wt7dnAIrz+MPi6SrzEP0IA+fgCa+Cdb2e9DtIh+ivuG9VkgGiYLohvqiwHC8kC+/M9PQCwm2pcFtBvRI4K2YbVfdjL1hfMFAqX9Mw4CgT4T/kDgjYW/3021uS4l+lk/1Njly6mCd7lIwXsYIMB53h+YCASCL7xRsLlWIXpEr/2832ofIvVOCt5N9AE/j/txvvyBYDA4+Wbm11uygNYjmkS/sA8ODRH/uFP28WL7jPt9GIjBCU5OvVlgQKtAVIl+BSOii/jHRRZoH8ND7ANAk5OTU1Oht/KPsKsRXaJfO4ZT/YKUl+85APIBEIMDPMGpqanJeaLVVLdBGaLXFhCNjs43DC9uGAzOBPg5OBEMvjA1CTjT09O38m2DhGwUM/HvBUS/JfNPKl94/QEgyFdwPmGh0HRo5la+jWI1ok30OzL/EJ7U+hMITBAajAMKzcwwGlXTPWzIR/R7d6q+vLhf4PU55WcosFDoyjTmmQmHb+c+bBBwHJOX6I/p9Xk8ZaCUoRk/Y54w8ESit3Mexwga8/NqROYf4h/saLAzU2DpfIUjV6PR8NcoH+kVIPpT2s/M8hzAyyHxM+gTAn0iENHYpygfehYkIvowBoL6ApoglucK1icM+YpEw9HYRykfCxck+jOZf8A+TIFNTZL6AhycsEg0Go19axXlg3MWIjL/ED/j9TlTX+FIGHhin6X9aCFH/CdDdP1F0sBS9UXsHJphaCKYJ/ahfA87DlIk+u8CjV4k8096PbyC5ZkJXyX5isW+Qf3xFBvR9b/60w01Xe4zjH3Az7F4/JPUH+DlIbqeIXqJzD/YP+DnaVJfjEDX4t/5APVHnOxEr780306hn2I/MzwxLNAX6D8E5kRE5p9QuryY+roGPIkP0n9Mnp/o9TTQjb+n5h+cr2mCEwGceOKLIrxIwE504+X5+QfrE8b2YQwdS3xYhFctWIluvLxg/knbOQY0icRXxHgZhY3oxt8WzT8kYVBfkLDEx9hej9lBnwjrs2j+gf4eBZxEPJH8vCgvNLEQ/SNr/sH1jgss+e33sr9itZE2EHp7eun8E41jnHgy+QlxXopji7mZJfNPLI4zlkx+ndObjGskIhAtmn8ACOormfzuR0R6sZIDUXjh/EPqK5H8tFivnnIhiiyYf4h/Zr/K+SJMeYMIRNH5+ecalieR/Ob7RHt9mRtRLD3/AA84+nsfF+8Fb+5EUSIP5Cv5GRFfgedMFCP9FBN9jueVHFEuCcwxfsY4yS/xvpAjyjWKuQTD88rsE3eXyEWTuTijz1P3lsxVnLnZeHL2qfeX0GWlO7PJJ+4tKzJEuc5158t3lxUdpXbhrfSuBJbepUna10rLyyhEqV28Lb2ryVikTcIvb2+ieHkb7452CuPZSfd6ewl+AKAEP5FQgh+RYE79KnnNAIdE/swGOT0uqQ+RkJ5bWp9qST3NKqWP2WSeHFdsqKqprU9/7qe+tqZqA6XP/fwfc5W5R7aUF8sAAAAASUVORK5CYII=)
            2x
        );
      }

      body {
        background-color: #ffffff;
        color: #646464;
      }

      body.safe-browsing {
        background-color: rgb(206, 52, 38);
        color: white;
      }

      button {
        background: rgb(76, 142, 250);
        border: 0;
        border-radius: 2px;
        box-sizing: border-box;
        color: #fff;
        cursor: pointer;
        float: right;
        font-size: 0.875em;
        margin: 0;
        padding: 10px 24px;
        transition: box-shadow 200ms cubic-bezier(0.4, 0, 0.2, 1);
      }

      [dir="rtl"] button {
        float: left;
      }

      button:active {
        background: rgb(50, 102, 213);
        outline: 0;
      }

      button:hover {
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.5);
      }

      #debugging {
        display: inline;
        overflow: auto;
      }

      .debugging-content {
        line-height: 1em;
        margin-bottom: 0;
        margin-top: 1em;
      }

      .debugging-title {
        font-weight: bold;
      }

      #details {
        color: #696969;
        margin: 45px 0 50px;
      }

      #details p:not(:first-of-type) {
        margin-top: 20px;
      }

      #details-button {
        background: inherit;
        border: 0;
        float: none;
        margin: 0;
        padding: 10px 0;
        text-decoration: underline;
      }

      #details-button:hover {
        box-shadow: inherit;
      }

      .error-code {
        color: #777;
        display: inline;
        font-size: 0.86667em;
        margin-top: 15px;
        opacity: 0.5;
        text-transform: uppercase;
      }

      #error-debugging-info {
        font-size: 0.8em;
      }

      h1 {
        color: #333;
        font-size: 1.6em;
        font-weight: normal;
        line-height: 1.25em;
        margin-bottom: 16px;
      }

      h2 {
        font-size: 1.2em;
        font-weight: normal;
      }

      .hidden {
        display: none;
      }

      html {
        -webkit-text-size-adjust: 100%;
        font-size: 125%;
      }

      .icon {
        background-repeat: no-repeat;
        background-size: 100%;
        height: 72px;
        margin: 0 0 40px;
        width: 72px;
      }

      input[type="checkbox"] {
        visibility: hidden;
      }

      .interstitial-wrapper {
        box-sizing: border-box;
        font-size: 1em;
        line-height: 1.6em;
        margin: 100px auto 0;
        max-width: 600px;
        width: 100%;
      }

      #main-message > p {
        display: inline;
      }

      #malware-opt-in {
        font-size: 0.875em;
        margin-top: 39px;
      }

      .nav-wrapper {
        margin-top: 51px;
      }

      .nav-wrapper::after {
        clear: both;
        content: "";
        display: table;
        width: 100%;
      }

      #opt-in-label {
        -webkit-margin-start: 32px;
      }

      .safe-browsing :-webkit-any(a, #details, #details-button, h1, h2, p, .small-link) {
        color: white;
      }

      .safe-browsing button {
        background-color: rgba(255, 255, 255, 0.15);
      }

      .safe-browsing button:active {
        background-color: rgba(255, 255, 255, 0.25);
      }

      .safe-browsing button:hover {
        box-shadow: 0 2px 3px rgba(0, 0, 0, 0.5);
      }

      .safe-browsing .error-code {
        display: none;
      }

      .safe-browsing .icon {
        background-image: -webkit-image-set(
          url(data:image/png;base64,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)
            1x,
          url(data:image/png;base64,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)
            2x
        );
      }

      .small-link {
        color: #696969;
        font-size: 0.875em;
      }

      .ssl .icon {
        background-image: image-set(
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABICAMAAABiM0N1AAACClBMVEUAAADbRTfrTjvcRjraQjbcRDjbRDjbRTfaRDXZQDPZQTTbQzfaRDbcRDfbQzbVKyvZQzXaQzbaRDbIPjLaRDbYQzfXQTfaQzbZQzbbRDi/QADbRDfbQDfbJCTcRTjbQzbIPjPbQzfbQzfbRTfTQyzcRzvbQzbaRDbaQjfbQzbaQzbaQzbaRDfYQTTaRDfbQzfaRDbaQzbbQjbbQjbZQjTZQzbaQzbYQTTVQTXbRDbPQDDbQzbIPzPbQzfbRDfbNzfZRDaAAADVOSvYQDbbRDa/QCDZRDbqVUDaQTPbRDfGPDLbQjXHPjTVQEDJPTLGPTHKPTPYTjvGPDHbRDe+Oi+6OS64OC7LPzLHPTL7+/urNSv5+fm/OjD4+PjEPDHFPDG5OC67OS/DOzG8OS+9Oi/COzDrn5nAOzDtoZvBOzD9/f36+vq3OC62Ny339/fIPjLsoJr+/v6xNizx8fHFPDCnMymjMii1NyyfMSfz8/PUlI+uNivLlI+oMynDPDDUlY+zNyylMiipNCrOlI/JPjLHPTHKPjKhMijPlI+3OC2+Oy/FPTH29vaqNSq5OS319fW8Oi7AOy/BOy+sNSv////VlZD8/PzQlZDKlI+iMijCPDDYmJO0NyykMiiwNiy2OC27OS69Oi6gMSfYl5K4OC3MPzPempXBPDDqnpjy8vL09PTHPjLRlZDbmZMWYj36AAAAUnRSTlMAgQ1CaODzz4soSuj4/tkGV9303/FBM9ic8gTpHAffhc+MKtAXQbDHdMaudtc7rX7q+n93Nl/VJyu4EK9B9vwOXgISNOIIgAw32vJNgAz+84ENOFEUuAAAA3VJREFUeF7t1mVvG1sQBuA6cRymQrBtUkpSZma6jAtmZg4zM5SZmS7+x85M1r5ptRuds2o/XCnz9UiP34GVvOrr1EqtVF2Vsaa5urikpLi6ucZYVaeTKSyoFz+p+oJCHcz6JlGlmtbzOsa1omqtNfI5DaJmNfA4BzLArk0Vm7du2LB1c0XBkYy0l90pUpjju5fq3+1QpCJWp/x7Yk4f/vzhx30ElZUzQi3k7Ff54WPFJLUwQmUEHVR7uniGIjEeIjmXLqs+bqLHo0zQToK+UX88UYLQTiboJEHrNF73ILSDCdpO0FkN6BxC25mgSoK0VnwIoUomaDVB5zWgCwitZoJEquWf/39QjiHfJDKVaYshR9vZtlHkqLxcTadU5KpSDelbysOVSb07g8hdBlUonx/KV4VM/FCtxoHw1xeDVqBodCkQDuuFonfvLpHCDsd7PRA57e0oKY7L4XqjEwIp3pbN43C5Hvr0tQZOHCUlT/phX8+CvmEjZAMpnCDndc/4cETX+tvi8fu2RBj6Imd2vHvC/oEbIum+zZZI4Hhc5Njtgx1X9EBi2GZz0JxhPphn8PlYapobIgnzkPOse+LanY7eVK95WhdEedJDkMd+bbBj7GkyaTa38kOKk746CfO5A32hY/b+zQuRkwbn6o056GsslQJm3uuVp/ggukPX0BA4N/56gHleYB5Z9gVm2CHKg07f7CRC/aNKX97rvkAgaGGHlHvuezTePQdOf/8oMBjI5wvclCQLG0QO5aF9/QPOn50DMB8ZnGBQkpxOCyP0BzYGeXroDkfB6bwHfcnXAwFynJKFsbV/oS/KY8c7vNdJgWDOweBNdCKR0DvGYT/B7x3uGb+L3uTAAI2H8khOKRILhfys65cxDzmwrnmacwDnQ3luhfzMkLgwPKF8F5n7wX2hhHncbmZIjMB8MA+WDPfzEvK8wjzojHBA4mN0ktBXdu8SOLFb4EBxQOIV5Z7fYl/EQF8xvz/kdnsEZogkOmevMh8n7isGcwbH06UK1WpJregofYGUdQThB85/bK3Ylwx3SI2Bg32NCEJXI+9/yFZZucMI5rmt5BGsP6lCOXna0hQ4mQHRvjwea5d1zc+rVCu3VFuaoXtevEP/CDqC9ZdTAKhLy2SyAJTdl1voEqxrNBzqzrDFpCnRPd8GBhzh18bfftdAPgL34oNsidB5lQAAAABJRU5ErkJggg==)
            1x,
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJAAAACQCAMAAADQmBKKAAACx1BMVEUAAADcRDfbSDjbRTfbRDfhSzwAAADbRDjbRzjbRTjbQzbaRDfaRDbcRDfTQyzXQzbZQDPbRDfcRDfbRTm/QCDaQzfbQzbaQzbMMzPbQzfbQzXaQzfeRjrbQjbVOSvbRDfaQzbaQzfFPDLZQjfZQzbVQCvZQzXaQjXaRDbXQTfbQzfaQTPZQTa/QADaQzbcRDjZQjXaQzfbRDTaQzbaQzbbQzfbQzfaRDfbQzbHQDTMMzPbNzfaQjfbQzbaQzfbRDbWQDTZQzfaQDXEPTHXQTbGPTHbRDbYQTTVRDPaQzbaRDXaQTXZQzXbRDfXQDDXRDTaRDbbQzbGPDLHPTPZQjTbRDfPQDDbRDbYQjbbRDbaQjbZQjbaQzfaQzfaQzXaQzbbJCTDPTDFPTTFPDLaQzbbRDbbPTHLPDXbQzbbQzfbRDfgSTnSPC3EPTHbRTfbQzbbRDfbQzbaRDfEPTHFPDLaQzbGPTLaQzatNiuiMiioNCntoZuuNivsoJrLlJCxNiy3OC2vNizz8/O3OC7Ok47+/v7x8fHWQTXMk4+9Oi739/f19fXw8PD29vb09PSlMymfMSfZQjW1Ny2zNyy7OS6nNCn4+Pjy8vKvNiu4OC2/Oy/WQjXYQjXMlI+sNSvVQTWpNCqjMimdMCfAOy/v7++4OC6+Oi/Rl5K1OC3////8/PzFPDHNk477+/u6OS7XQjX6+vq0Nyy5OC67OS+5OS29Oi/Qko3BOy+8OS/DPDCkMinSl5LPk47Rk46wNiy8Oi6/OjDAOzCeMCe2OC3CPDDCOzDDPDG5OS6sNCrEPTGyNizEPDGgMSfBOzD9/f3Qk46tNSvnnZezNizDOzHonpi0Ny2uNSvOlI+1Nyz5+fm7Oi7NlJDNlI/TmJOjMiioNCqqNCq4OS3Oko3MlZDVQTSrNCqmMynPko2sNSrQlpGhMijFPTHbRDeKorW+AAAAeHRSTlMA2UCB7CIB8zLIt8j4vhcTFPzYVQjk/qQF95TJVFUS+p37vl16DDVh6jOoNy8Eir9luzHC4+gqte9ACg6DhZmpLJUw80eB0yce3XxSV+kgQFrF+jI2zBC4QvBZUZ/ffcEH2VTHq/0VIpu2sTER2cewYmOe7Nj67Nj6WWwvAAAIQElEQVR4XuyVWWvqUBRG++RDIlHBqIkoinMnnDrg2BZROw7gPLR9ULG9F9p7QfzT+0f0cSe11RzZSV/Oel8fK2w42TEIh8PhcDgcDqeQipQr1a64PFKUo6XYrVbKkVThl2KcAbXugW/w1NWA0+oaRzrjgjW4MmmHhTlnITtsxB46syjn+AQMcnJsQU5QDYNhwmrQ7J57GZiQ703NsZWmwMi0ZDOvx+eFLfD6zOpxC7AVgtuke01gFbv/PFHba0gvL1Jjr5Y499thlYk5VzuEr1xeZVfO4cteXcJXDs3ouQY9irf3w4fbel4F9FzT9zhvQYdwt064E0DHLf3PbRe0JB82CQ9JnbBL3RMHLY+OzYbjUafEiYN0JxCLRpSiX+u80va0QEO7Y0zqtLVWizRoDoj816gVlAGZk77RfUAGxr0BIH3K9/oGkByLmAPkhjBohLOufRZx34XmiDBojLPvbOYbmmO6niYgH2zqP0CaZEEBHPVIbKrkQTdAFhTFUZHVFdGNkgX9x9EnVvcJ3RBZ0DOODlndIbrPZEFLHL1gdS/QXZIF5XF0xurO0M2TBZ3iaIzVjaF7Sha0wNEDVvcA3QVZECDWyjyIB/EgHvTnk506Vm0cCMIAfLJsZBdu7lpDHiFvltqytDZXCJcxdxgOVOjsLguGvVZFClUqFkHAKdJESmFBxD7E7Y6NdLAILHM7lf4n+Jj5Z+yp5Yj/F8ea2uPbObOvwkSs2W2c0YMwlcnoBs9gKMxlOOjuuRMmc9dVNBoKsxl23NpEmM6k230J8/nWBWQhgKwOnrHASIcPaaOA7OtBUxTQvYEKYZXIQQE514METnpQD+pBZtODepDntQMIwQd5T0+tIkIpwQWBp1VEaEYPR0wQeFpFJKOUHkCEBAJPq4gA58DYEQ8Enkak7+ssekEHgUjbF3gYY2+fIQpIF+n9kRrGlvsiRAHpIt0jRcskSdIQC6SLGg8MSHk2nBchAqhV1HgYeDa8qtIQC6SLSKYKzS4emapy3fh7hADSRIF39hwAJD37JOGcS08c+xEWqBEFQeARqiI1tadyFahcPEdYIOHVoCyr+wOeDVeg9/hRgharCAPUiALlodnF88Zkf3giObGM8vzOQYQBAlGgQLSej/LAvhTosSwXeVGcfkZYIOEpDgzon3uXnmqn+lOWufKk6Z8ICQQi4KjU/5BXOzUf2FdxkqD5jwgLJMilzwz6s4d/CJ5yu81z8Mzn/q/XNRqorg8MCPqzc6E+W7mvIj2lvu8/rz7WOCBC64P/W7v57LZRRlG8/BOwYNUHQOoLdM0a9QXoE7QsWLECodZy42JXmdZxTI2dOA20KgQPES0DYzPJJCTuDINp62EIqqWSQlALoQWVPgT33qOPGdlxwNH33Sf46Zxz75zFN/fuzc/vEo8sGPEgP6TPqYVut9C/aRkHyvYf8MyXdx+r9crlHiA/jFPouy40MguUfk8BVC7PXl4nv9bn5uau3n/44OEVkof86vb7ddd1LNNA4IFfNGUh+oXv8yPJ8y02rCs8rutGkW+ZBcr2H9GHcGZnZs6zXVfhF8WZgAhn2d0utVogMgMEHrXwU1PgKc/OzFZ3cjm176QP7HKjVuksiAwB4QCl93mKeUggmup1wiGev0SfPvsV0bRo2p5lCAg8AELf2CUeBqrOVIvXkZ88LRjyAxwCugQi/UCq/wgPvqeXRZ9qtVosFs9xnFmgQpbnbLvtOLZlAEjpI0DoP3QPd9gv4Wk2NwhI9t1lnhLBsD4EBCK9QODJ9p+L6D/nSR7wTDc32C7iQZ5B077kdGhApBEI3wsmGu4/O8TDQNM0W/DLXY4ikQf6dJyO7wd/aASCPiP9B9/TRz9BH5pKZQv7tV1K80MC+R3f8wJLMxDus/q8E4/UVe4/51if5nSFZhP3h2Fa7ZYYxo55vnfDCy2tlv2ayQ/0kfos/WeDBSKgT1awXy0lkOjj+D4J5Nn2oqUT6INPab0+F79G+8/vhCM89brL5zBCfhwGYpyGZ/MkljYgEKX5OT3UfzYqRLSJ81OCOio/kOcCAwWJLiAQfc08LFDaf+6r/rNVqawwz3JUYnkUDgvU8DyhCYIw1AcEoqlvLhIO5Zn7Tw79R+phvrvyJ/mVfi8kzl91OowDoAtBYOsDwnxxRd0f7j+SZ3y/Mv0HftHIemX9CkKtCoHoR9IH+WG7RvoP8gN5iEaAIA94dAJhPryr8pz2H/QNV/UfBAgL5vkNWyYgoMUw0RtqEC2Ah/wa23/S/UKeEWjCSZb0AoGoIAuWzY/qPyXVf9ocZwf5gV92GC4mSa+nGwhEuM+y7nnpP3fqQ/1H5VlooE/IPAPdQCCqU59X+uzZfzoO9LlhY4IA+qzqVwhE7xOP7JfqP8sj/cf3WCDcn5AD1GOBDCgEooj1wX4VkOfScP/xGhl5GGhpMDACBKLfmGeBgMb3HxxE7Bfx0Ax6sbHHKLWbt4SnsGf/8aX/wDAJdC9JVsmw+FVzz3VqjXz3XdKnPq7/MAz0oTwnrA8J9Ob/Bzr6ZGIikkf1H+THGe4/AQMxzhLhDOI4PmLyyVft58LY/sPqZPLDI0DHjD6Kq3n/3X9sEmipJ/rQXDtu9tlgzXZdwZE8p/3HTvtPyDgAWovjE4cmmMNPDkAU/tt/nL37D+K8OohFoJPGn57Wvt23/wCI7VpjntcNP84F0Zj+E6D/JHKfY5m33jD8fBlE3+3bf0Qf+PXaK+YfeINofP9J47x27R3wTOjagXJ0e5/+w+c5lvzAr4nn8FMHIRrbf5Rhb2O/DjQvTP4bRe3vcf2Hv6cnjhw7PjnGP0i3E4uinqkcAAAAAElFTkSuQmCC)
            2x
        );
      }

      .captive-portal .icon {
        background-image: image-set(
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABICAQAAAD/5HvMAAAFDElEQVRo3u2afWhWVRzHz2bNkhRDKyRb6WxiK5m1sP5YDXoZT9tzn3u+P8voBVy4iCyaQkqBrkZJRUhQMYPUyjmQcsNeEFs10KEbKr1YA6M0Z24Mp8IM99TjdvvjOc997vu597n3WQt27j9j55x7P8/v/M7v/F4OY5Ntsk22yfY/a8p0NcbX0RZ04TcM0kWkcB59OIp2vMnreKnjpEK1HA1owxH00QhdoOPoQQtWKgtCodDNeAUHkSLN68Fp86zYNViPftfRvfyZ+LTAKGVFWEnd3iDZxyhNvEsj0hnn+Do2xTfM3Veigf70C2MEomo6aeoZxTHaR7uwGwfxh2XW4cRt/pZJtU31CRSbil59YZLYCh6fR9VYgbW0Rn2C36uW4El8jjF9TJsUJj4bXwaFMUpILcEQaUjidZqP59FDl0zjRtCB5YlbsI000ugnZbpsNy3GiVxwjDqUqMR+fiutobOuSn2Cg+5HD26U4HDQX7nhGIEYKyuifbLx2CxbqwLakF3bcECMYa2u0h30IlUrS3Anr0UTHRL/v6TGvHEKsSN3GDsQY/QRaWjhi7AMH+MYhpHEKXyFBtRQJ2l8tWxfNYfDsQOVFan3gVtMgEYaXcRGUiU4aAyLYwdirOoy6nQxiaXe0nkojO64AzGmzqSfSSMNwzhAe3E6bZ0SlZ44iRswFB7HGYixeDGO8LrEUr6KP8VLlQrsx3LZcnVEgeMGxBibgrbMjuOvSe0yfzQaHOtpb/rJL4sxY7xW6uW4uwgBn1ZPC7eLNNJog1Q+eCkinLOYK/nhvdjNCmTH6DSciWCx+qnVG4cxxpQFsRlyJ+OFSJU3fKMfJxSQWh7x9g7b+FviE/9MECD8kP4Af5X+ngBA8dni/BpVZ+KxIGdZKCFsFm95w8k3THcdMrlTeQbiD4u3dNtZ14uuTWLHvTcuEpojbNewvUv4h7xe9xjbx0OHcN7lLRnfFvcYQsMD+VfiTCRsJxXBjnqTSdF/zTcQPnUDEk4Zn2Xin4/BPEtoi9uSCdtTVmQ5BCuskVnE5vidgECMocYc/I4TkPOSiUn1/8GSOSm1obcpoE90ShaHSpXavu0tE7cFROoLu+2thtHS7ric9ubDC3A1jNajw8kPpu+jBvI4OsyHq9v0IHm0kIer0f3weMEiOhephNzdj6yDpj7iGWhXIhkZUIG+tx/0cmG/kInZn/sm50lUZhIyjjnqjJOPFL9WgrQ6GiB8KL64QxIG4W2p9YgAKF6sJ9OrJYEikrJsaBRA+ESMPOmav8+G0mjJN5BantFEvspHsgFjuD0skHguUDevt6cV8LXoH6i6wl86ptMrNxE4AfEt5lhcmkzPs74TVtjoIcn+4EjZH6iW6Dn9w6xQvhn1lB5/3FVCrTlkAZ4W5ZgZejlmVKnwYT4NSc8R3OUCPTeHxGi3yDDu0aXW6NeLy6aFB9wMQO31tB19SFlqO57qbXRZSaNvfCyXQ+J8wE1KwRU8NlW3PRodl50HrqUFJLEiGiD06H8NBi/8mosvm9yroTlkIYeUJbkEBAVoNJQeuxJLI7JJR+Pzco+aTAU8fKYsDAuE9qqrwl0YMJU4kcIH8eLcgdAkzU37yq2ZisAYw3e8TrkuKBDOEEUXXzqVyX+hZnqOP+ALZ5Saa66ONOQNfpHAALNTWZyXxGiwqxbpDY73JdXCCJbP52UU2s4T9lxK3lr6ug62ogu/26/rOJmHYO1faMmeMhUfGLMAAAAASUVORK5CYII=)
            1x,
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJAAAACQCAMAAADQmBKKAAACfFBMVEUAAABSUlJSUlIrKytSUlJTU1NAQEBSUlJSUlIAAABTU1NTU1NSUlJTU1NSUlJTU1NQUFBSUlJQUFBTU1NTU1NSUlJTU1MAAABPT09SUlJSUlJQUFBRUVEzMzNSUlJTU1NSUlJTU1NQUFBPT09SUlJSUlJSUlJRUVFSUlJRUVFTU1NSUlJTU1NAQEBTU1NSUlJTU1NTU1NTU1NJSUlPT09OTk5SUlJPT09TU1NRUVFSUlJTU1NKSkpTU1NRUVFPT09RUVFSUlJOTk5SUlJSUlJSUlJRUVFSUlJSUlJGRkZRUVFSUlJOTk5SUlJTU1NRUVFQUFBTU1NSUlJHR0dOTk5SUlJSUlJPT09SUlJTU1NRUVEAAABRUVFSUlJNTU1TU1NTU1NSUlJTU1NTU1NTU1NRUVFRUVFTU1NOTk5SUlJTU1NAQEBRUVFTU1NSUlJTU1NQUFBSUlJSUlJTU1NTU1NSUlJSUlJSUlJTU1NSUlJTU1NQUFBSUlJSUlJTU1NTU1NSUlJSUlJSUlJSUlJQUFBTU1NTU1NTU1NSUlJTU1NLS0tSUlJQUFBSUlJTU1NNTU1SUlJRUVFSUlJSUlJSUlJSUlJTU1NSUlJSUlJSUlJTU1NTU1NTU1NRUVFTU1NSUlJTU1NSUlJSUlJSUlJTU1NTU1NTU1M5OTlQUFBTU1NSUlJSUlJQUFBTU1NQUFBTU1NSUlJRUVFSUlJSUlJSUlJSUlJSUlJTU1NSUlJNTU1SUlJSUlJSUlJERERRUVFRUVFSUlJRUVFSUlJRUVFRUVFRUVFSUlJOTk5RUVFSUlJJSUlSUlJSUlJRUVFSUlJSUlJSUlJMTExSUlJTU1MPbK0hAAAA03RSTlMA/uwG+/kE6doCwszG85X6IEtDudLEiwE3H7IQFgV87d/UST0crLssjDkr+KkM3jiz9CIVHQ2oOoher+oYckIqZfI0iT6rhNm1C1vvJIaOazD9hRIaw90tgsWHA3G9IduwMvzn1RNf9hfAUwh0frhHXOZ52Mhz5WD3ruFWocFKdZxU1ztAl6140L8RtDNOaQoZYeB/Z13w4/W6bOSUjaOWoFen4stvnQk2poPHI5FZmspi6301krHuWh52n+gPWE9qJp4vkEWbJzxwDphkgcmApRtj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)
            2x
        );
      }

      .styled-checkbox {
        float: left;
        height: 16px;
        margin-top: 0.36em;
        position: relative;
        width: 16px;
      }

      [dir="rtl"] .styled-checkbox {
        float: right;
      }

      .styled-checkbox label {
        background: transparent;
        border: white solid 1px;
        border-radius: 2px;
        height: 14px;
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
        width: 14px;
      }

      .styled-checkbox .checkbox-tick {
        background: transparent;
        border: 2px solid white;
        border-right-width: 0;
        border-top-width: 0;
        content: "";
        height: 4px;
        left: 2px;
        opacity: 0;
        position: absolute;
        top: 3px;
        transform: rotate(-45deg);
        width: 9px;
      }

      .styled-checkbox input[type="checkbox"]:checked ~ .checkbox-tick {
        opacity: 1;
      }

      @media (max-width: 700px) {
        .interstitial-wrapper {
          padding: 0 10%;
        }

        #error-debugging-info {
          overflow: auto;
        }
      }

      @media (max-height: 600px) {
        .error-code {
          margin-top: 10px;
        }

        .interstitial-wrapper {
          margin-top: 13%;
        }
      }

      @media (max-width: 420px) {
        button,
        [dir="rtl"] button,
        .small-link {
          float: none;
          font-size: 0.825em;
          font-weight: 400;
          margin: 0;
          text-transform: uppercase;
          width: 100%;
        }

        #details {
          margin: 20px 0 20px 0;
        }

        #details p:not(:first-of-type) {
          margin-top: 10px;
        }

        #details-button {
          display: block;
          margin-top: 20px;
          text-align: center;
          width: 100%;
        }

        .interstitial-wrapper {
          padding: 0 5%;
        }

        #malware-opt-in {
          margin-top: 24px;
        }

        .nav-wrapper {
          margin-top: 30px;
        }
      }

      /**
 * Mobile specific styling.
 * Navigation buttons are anchored to the bottom of the screen.
 * Details message replaces the top content in its own scrollable area.
 */

      @media (max-width: 420px) and (orientation: portrait) {
        #details-button {
          border: 0;
          margin: 8px 0 0;
        }

        .secondary-button {
          -webkit-margin-end: 0;
          margin-top: 16px;
        }
      }

      /* Fixed nav. */
      @media (min-width: 240px) and (max-width: 420px) and (min-height: 401px) and (orientation: portrait), (min-width: 421px) and (max-width: 736px) and (min-height: 240px) and (max-height: 420px) and (orientation: landscape) {
        body .nav-wrapper {
          background: #f7f7f7;
          bottom: 0;
          left: 0;
          margin: 0;
          max-width: 736px;
          position: fixed;
          z-index: 1;
        }

        body.safe-browsing .nav-wrapper {
          background: rgb(206, 52, 38);
        }

        .interstitial-wrapper {
          max-width: 736px;
        }
      }

      @media (max-width: 420px) and (orientation: portrait), (max-width: 736px) and (max-height: 420px) and (orientation: landscape) {
        body {
          margin: 0 auto;
        }

        button,
        [dir="rtl"] button,
        button.small-link {
          font-family: Roboto-Regular, Helvetica;
          font-size: 0.933em;
          font-weight: 600;
          margin: 6px 0;
          text-transform: uppercase;
        }

        .nav-wrapper {
          box-sizing: border-box;
          padding: 16px 24px 8px;
          width: 100%;
        }

        .error-code {
          margin-top: 0;
        }

        #details {
          box-sizing: border-box;
          height: auto;
          margin: 0;
          opacity: 1;
          transition: opacity 250ms cubic-bezier(0.4, 0, 0.2, 1);
        }

        #details.hidden,
        #main-content.hidden {
          display: block;
          height: 0;
          opacity: 0;
          overflow: hidden;
        }

        #details-button {
          padding-bottom: 16px;
          padding-top: 16px;
        }

        h1 {
          font-size: 1.5em;
          margin-bottom: 8px;
        }

        .icon {
          margin-bottom: 12px;
        }

        .interstitial-wrapper {
          box-sizing: border-box;
          margin: 24px auto 12px;
          padding: 0 24px;
          position: relative;
        }

        .interstitial-wrapper p {
          font-size: 0.95em;
          line-height: 1.61em;
          margin-top: 8px;
        }

        #main-content {
          margin: 0;
          transition: opacity 100ms cubic-bezier(0.4, 0, 0.2, 1);
        }

        .small-link {
          border: 0;
        }

        .suggested-left > #control-buttons,
        .suggested-right > #control-buttons {
          float: none;
          margin: 0;
        }
      }

      @media (min-height: 400px) and (orientation: portrait) {
        body:not(.safe-browsing-has-checkbox) .interstitial-wrapper {
          margin-bottom: 145px;
        }
      }

      @media (min-height: 299px) and (orientation: portrait) {
        .nav-wrapper {
          padding-bottom: 16px;
        }
      }

      @media (min-height: 405px) and (orientation: portrait) {
        .icon {
          margin-bottom: 24px;
        }

        .interstitial-wrapper {
          margin-top: 64px;
        }
      }

      @media (min-height: 480px) and (max-width: 420px) and (orientation: portrait), (min-height: 338px) and (max-height: 420px) and (max-width: 736px) and (orientation: landscape) {
        .icon {
          margin-bottom: 24px;
        }

        .nav-wrapper {
          padding: 16px 24px 24px;
        }
      }

      @media (min-height: 500px) and (max-width: 414px) and (orientation: portrait) {
        :not(.safe-browsing-has-checkbox) .interstitial-wrapper {
          margin-top: 96px;
        }
      }

      /* Phablet sizing */
      @media (min-width: 375px) and (min-height: 641px) and (max-width: 414px) and (orientation: portrait) {
        button,
        [dir="rtl"] button,
        .small-link {
          font-size: 1em;
          padding-bottom: 12px;
          padding-top: 12px;
        }

        body:not(.offline) .icon {
          height: 80px;
          width: 80px;
        }

        #details-button {
          margin-top: 28px;
        }

        h1 {
          font-size: 1.7em;
        }

        .icon {
          margin-bottom: 28px;
        }

        .interstitial-wrapper {
          padding: 28px;
        }

        .interstitial-wrapper p {
          font-size: 1.05em;
        }

        .nav-wrapper {
          padding: 28px;
        }
      }

      @media (min-width: 420px) and (max-width: 736px) and (min-height: 240px) and (max-height: 298px) and (orientation: landscape) {
        body:not(.offline) .icon {
          height: 50px;
          width: 50px;
        }

        .icon {
          padding-top: 0;
        }

        .interstitial-wrapper {
          margin-top: 16px;
        }

        .nav-wrapper {
          padding: 0 24px 8px;
        }
      }

      @media (min-width: 420px) and (max-width: 736px) and (min-height: 240px) and (max-height: 420px) and (orientation: landscape) {
        #details-button {
          margin: 0;
        }

        .interstitial-wrapper {
          margin-bottom: 70px;
        }

        .nav-wrapper {
          margin-top: 0;
        }

        #malware-opt-in {
          margin-top: 0;
        }
      }

      /* Phablet landscape */
      @media (min-width: 680px) and (max-height: 414px) {
        .interstitial-wrapper {
          margin: 24px auto;
        }

        .nav-wrapper {
          margin: 16px auto 0;
        }
      }

      @media (max-height: 240px) and (orientation: landscape), (max-height: 480px) and (orientation: portrait), (max-width: 419px) and (max-height: 323px) {
        body:not(.offline) .icon {
          height: 56px;
          width: 56px;
        }

        .icon {
          margin-bottom: 16px;
        }
      }

      /* Small mobile screens. No fixed nav. */
      @media (max-height: 400px) and (orientation: portrait), (max-height: 239px) and (orientation: landscape), (max-width: 419px) and (max-height: 360px) {
        .interstitial-wrapper {
          display: flex;
          flex-direction: column;
          margin-bottom: 0;
        }

        #details {
          flex: 1 1 auto;
          order: 0;
        }

        #main-content {
          flex: 1 1 auto;
          order: 0;
        }

        .nav-wrapper {
          flex: 0 1 auto;
          margin-top: 8px;
          order: 1;
          padding-left: 0;
          padding-right: 0;
          position: relative;
          width: 100%;
        }
      }

      /* Malware opt-in. No fixed nav. */
      @media (max-height: 600px) and (orientation: portrait), (max-height: 360px) and (max-width: 680px) and (orientation: landscape) {
        .safe-browsing-has-checkbox .interstitial-wrapper {
          display: flex;
          flex-direction: column;
          margin-bottom: 0;
        }

        .safe-browsing-has-checkbox #details {
          flex: 1 1 auto;
          order: 0;
        }

        .safe-browsing-has-checkbox #main-content {
          flex: 1 1 auto;
          order: 0;
        }

        .safe-browsing-has-checkbox #malware-opt-in {
          margin-bottom: 8px;
        }

        body.safe-browsing-has-checkbox .nav-wrapper {
          flex: 0 1 auto;
          margin-top: 0;
          order: 1;
          padding-left: 0;
          padding-right: 0;
          position: relative;
          width: 100%;
        }
      }
    </style>
    <style>
      /* Copyright 2013 The Chromium Authors. All rights reserved.
 * Use of this source code is governed by a BSD-style license that can be
 * found in the LICENSE file. */

      /* Don't use the main frame div when the error is in a subframe. */
      html[subframe] #main-frame-error {
        display: none;
      }

      /* Don't use the subframe error div when the error is in a main frame. */
      html:not([subframe]) #sub-frame-error {
        display: none;
      }

      #diagnose-button {
        -webkit-margin-start: 0;
        float: none;
        margin-bottom: 10px;
        margin-top: 20px;
      }

      h1 {
        margin-top: 0;
      }

      h2 {
        color: #666;
        font-size: 1.2em;
        font-weight: normal;
        margin: 10px 0;
      }

      a {
        color: rgb(17, 85, 204);
        text-decoration: none;
      }

      .icon {
        -webkit-user-select: none;
        content: "";
      }

      .icon-generic {
        /**
   * Can't access chrome://theme/IDR_ERROR_NETWORK_GENERIC from an untrusted
   * renderer process, so embed the resource manually.
   */
        content: -webkit-image-set(
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABIAQMAAABvIyEEAAAABlBMVEUAAABTU1OoaSf/AAAAAXRSTlMAQObYZgAAAENJREFUeF7tzbEJACEQRNGBLeAasBCza2lLEGx0CxFGG9hBMDDxRy/72O9FMnIFapGylsu1fgoBdkXfUHLrQgdfrlJN1BdYBjQQm3UAAAAASUVORK5CYII=)
            1x,
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJAAAACQAQMAAADdiHD7AAAABlBMVEUAAABTU1OoaSf/AAAAAXRSTlMAQObYZgAAAFJJREFUeF7t0cENgDAMQ9FwYgxG6WjpaIzCCAxQxVggFuDiCvlLOeRdHR9yzjncHVoq3npu+wQUrUuJHylSTmBaespJyJQoObUeyxDQb3bEm5Au81c0pSCD8HYAAAAASUVORK5CYII=)
            2x
        );
        padding-top: 20px;
      }

      .icon-offline {
        content: -webkit-image-set(
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABIAQMAAABvIyEEAAAABlBMVEUAAABTU1OoaSf/AAAAAXRSTlMAQObYZgAAAGxJREFUeF7tyMEJwkAQRuFf5ipMKxYQiJ3Z2nSwrWwBA0+DQZcdxEOueaePp9+dQZFB7GpUcURSVU66yVNFj6LFICatThZB6r/ko/pbRpUgilY0Cbw5sNmb9txGXUKyuH7eV25x39DtJXUNPQGJtWFV+BT/QAAAAABJRU5ErkJggg==)
            1x,
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJAAAACQBAMAAAAVaP+LAAAAGFBMVEUAAABTU1NNTU1TU1NPT09SUlJSUlJTU1O8B7DEAAAAB3RSTlMAoArVKvVgBuEdKgAAAJ1JREFUeF7t1TEOwyAMQNG0Q6/UE+RMXD9d/tC6womIFSL9P+MnAYOXeTIzMzMzMzMzaz8J9Ri6HoITmuHXhISE8nEh9yxDh55aCEUoTGbbQwjqHwIkRAEiIaG0+0AA9VBMaE89Rogeoww936MQrWdBr4GN/z0IAdQ6nQ/FIpRXDwHcA+JIJcQowQAlFUA0MfQpXLlVQfkzR4igS6ENjknm/wiaGhsAAAAASUVORK5CYII=)
            2x
        );
        position: relative;
      }

      .error-code {
        display: block;
      }

      #content-top {
        margin: 20px;
      }

      #help-box-inner {
        background-color: #f9f9f9;
        border-top: 1px solid #eee;
        color: #444;
        padding: 20px;
        text-align: start;
      }

      #suggestion {
        margin-top: 15px;
      }

      #short-suggestion {
        margin-top: 5px;
      }

      #sub-frame-error-details {
        color: #8f8f8f;
        /* Not done on mobile for performance reasons. */
        text-shadow: 0 1px 0 rgba(255, 255, 255, 0.3);
      }

      [jscontent="failedUrl"] {
        overflow-wrap: break-word;
      }

      #search-container {
        /* Prevents a space between controls. */
        display: flex;
        margin-top: 20px;
      }

      #search-box {
        border: 1px solid #cdcdcd;
        flex-grow: 1;
        font-size: 16px;
        height: 26px;
        margin-right: 0;
        padding: 1px 9px;
      }

      #search-box:focus {
        border: 1px solid rgb(93, 154, 255);
        outline: none;
      }

      #search-button {
        border: none;
        border-bottom-left-radius: 0;
        border-top-left-radius: 0;
        box-shadow: none;
        display: flex;
        height: 30px;
        margin: 0;
        padding: 0;
        width: 60px;
      }

      #search-image {
        content: -webkit-image-set(
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA4AAAAPCAQAAAB+HTb/AAAArElEQVR4Xn3NsUoCUBzG0XvB3U0chR4geo5qihpt6gkCx0bXFsMERWj2KWqIanAvmlUUoQapwU6g4l8H5bd9Z/iSPS0hu/RqZqrncBuzLl7U3Rn4cSpQFTeroejJl1Lgs7f4ceDPdeBMXYp86gaONYJkY83AnqHiGk9wHnjk16PKgo5N9BUCkzPf5j6M0PfuVg5MymoetFwoaKAlB26WdXAvJ7u5mezitqtkT//7Sv/u96CaLQAAAABJRU5ErkJggg==) 1x,
          url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABwAAAAeCAQAAACVzLYUAAABYElEQVR4Xr3VMUuVURzH8XO98jgkGikENkRD0KRGDUVDQy0h2SiC4IuIiktL4AvQt1CDBJUJwo1KXXS6cWdHw7tcjWwoC5Hrx+UZgnNO5CXiO/75jD/+QZf9MzjskVU7DrU1zRv9G9ir5hsA4Nii83+GA9ZI1nI1D6tWAE1TRlQMuuuFDthzMQefgo4nKr+f3dIGDdUUHPYD1ISoMQdgJgUfgqaKEOcxWE/BVTArJBvwC0cGY7gNLgiZNsD1GP4EPVn4EtyLYRuczcJ34HYMP4E7GdajDS7FcB48z8AJ8FmI4TjouBkzZ2yBuRQMlsButIZ+dfDVUBqOaIHvavpLVHXfFmAqv45r9gEHNr3y3hcAfLSgSMPgiiZR+6Z9AMuKNAwqpjUcA2h55pxgAfBWkYRlQ254YMJloaxPHbCkiGCymL5RlLA7GnRDXyuC7uhicLoKdRyaDE5Pl00K//93nABqPgBDK8sfWgAAAABJRU5ErkJggg==) 2x);
        margin: auto;
      }

      .secondary-button {
        -webkit-margin-end: 16px;
        background: #d9d9d9;
        color: #696969;
      }

      .hidden {
        display: none;
      }

      .suggestions {
        margin-top: 18px;
      }

      .suggestion-header {
        font-weight: bold;
        margin-bottom: 4px;
      }

      .suggestion-body {
        color: #777;
      }

      /* Increase line height at higher resolutions. */
      @media (min-width: 641px) and (min-height: 641px) {
        #help-box-inner {
          line-height: 18px;
        }
      }

      /* Decrease padding at low sizes. */
      @media (max-width: 640px), (max-height: 640px) {
        h1 {
          margin: 0 0 15px;
        }
        #content-top {
          margin: 15px;
        }
        #help-box-inner {
          padding: 20px;
        }
        .suggestions {
          margin-top: 10px;
        }
        .suggestion-header {
          margin-bottom: 0;
        }
        .error-code {
          margin-top: 10px;
        }
      }

      /* Don't allow overflow when in a subframe. */
      html[subframe] body {
        overflow: hidden;
      }

      #sub-frame-error {
        -webkit-align-items: center;
        background-color: #ddd;
        display: -webkit-flex;
        -webkit-flex-flow: column;
        height: 100%;
        -webkit-justify-content: center;
        left: 0;
        position: absolute;
        top: 0;
        transition: background-color 0.2s ease-in-out;
        width: 100%;
      }

      #sub-frame-error:hover {
        background-color: #eee;
      }

      #sub-frame-error .icon-generic {
        margin: 0 0 16px;
      }

      #sub-frame-error-details {
        margin: 0 10px;
        text-align: center;
        visibility: hidden;
      }

      /* Show details only when hovering. */
      #sub-frame-error:hover #sub-frame-error-details {
        visibility: visible;
      }

      /* If the iframe is too small, always hide the error code. */
      /* TODO(mmenke): See if overflow: no-display works better, once supported. */
      @media (max-width: 200px), (max-height: 95px) {
        #sub-frame-error-details {
          display: none;
        }
      }

      /* Adjust icon for small embedded frames in apps. */
      @media (max-height: 100px) {
        #sub-frame-error .icon-generic {
          height: auto;
          margin: 0;
          padding-top: 0;
          width: 25px;
        }
      }

      /* details-button is special; it's a <button> element that looks like a link. */
      #details-button {
        box-shadow: none;
        min-width: 0;
      }

      /* Styles for platform dependent separation of controls and details button. */
      .suggested-left > #control-buttons,
      .suggested-left #stale-load-button,
      .suggested-right > #details-button {
        float: left;
      }

      .suggested-right > #control-buttons,
      .suggested-right #stale-load-button,
      .suggested-left > #details-button {
        float: right;
      }

      .suggested-left .secondary-button {
        -webkit-margin-end: 0px;
        -webkit-margin-start: 16px;
      }

      #details-button.singular {
        float: none;
      }

      #buttons::after {
        clear: both;
        content: "";
        display: block;
        width: 100%;
      }

      /* Offline page */
      .offline .interstitial-wrapper {
        color: #2b2b2b;
        font-size: 1em;
        line-height: 1.55;
        margin: 0 auto;
        max-width: 600px;
        padding-top: 100px;
        width: 100%;
      }

      .offline .runner-container {
        height: 150px;
        max-width: 600px;
        overflow: hidden;
        position: absolute;
        top: 35px;
        width: 44px;
      }

      .offline .runner-canvas {
        height: 150px;
        max-width: 600px;
        opacity: 1;
        overflow: hidden;
        position: absolute;
        top: 0;
        z-index: 2;
      }

      .offline .controller {
        background: rgba(247, 247, 247, 0.1);
        height: 100vh;
        left: 0;
        position: absolute;
        top: 0;
        width: 100vw;
        z-index: 1;
      }

      #offline-resources {
        display: none;
      }

      @media (max-width: 420px) {
        .suggested-left > #control-buttons,
        .suggested-right > #control-buttons {
          float: none;
        }
      }

      @media (max-height: 350px) {
        h1 {
          margin: 0 0 15px;
        }

        .icon-offline {
          margin: 0 0 10px;
        }

        .interstitial-wrapper {
          margin-top: 5%;
        }

        .nav-wrapper {
          margin-top: 30px;
        }
      }

      @media (min-width: 600px) and (max-width: 736px) and (orientation: landscape) {
        .offline .interstitial-wrapper {
          margin-left: 0;
          margin-right: 0;
        }
      }

      @media (min-height: 240px) and (orientation: landscape) {
        .offline .interstitial-wrapper {
          margin-bottom: 90px;
        }

        .icon-offline {
          margin-bottom: 20px;
        }
      }

      @media (max-height: 320px) and (orientation: landscape) {
        .icon-offline {
          margin-bottom: 0;
        }

        .offline .runner-container {
          top: 10px;
        }
      }

      @media (max-width: 240px) {
        button {
          padding-left: 12px;
          padding-right: 12px;
        }

        .interstitial-wrapper {
          overflow: inherit;
          padding: 0 8px;
        }
      }

      @media (max-width: 120px) {
        button {
          width: auto;
        }
      }
    </style>
    <script>
      // Copyright 2015 The Chromium Authors. All rights reserved.
      // Use of this source code is governed by a BSD-style license that can be
      // found in the LICENSE file.

      var mobileNav = false;

      /**
       * For small screen mobile the navigation buttons are moved
       * below the advanced text.
       */
      function onResize() {
        var helpOuterBox = document.querySelector("#details");
        var mainContent = document.querySelector("#main-content");
        var mediaQuery = "(min-width: 240px) and (max-width: 420px) and " + "(orientation: portrait), (max-width: 736px) and " + "(max-height: 420px) and (orientation: landscape)";
        var runnerContainer = document.querySelector(".runner-container");

        // Check for change in nav status.
        if (mobileNav != window.matchMedia(mediaQuery).matches) {
          mobileNav = !mobileNav;

          // Handle showing the top content / details sections according to state.
          if (mobileNav) {
            mainContent.classList.toggle("hidden", !detailsHidden);
            helpOuterBox.classList.toggle("hidden", detailsHidden);
            if (runnerContainer) {
              runnerContainer.classList.toggle("hidden", !detailsHidden);
            }
          } else if (!detailsHidden) {
            if (runnerContainer) {
              runnerContainer.classList.remove("hidden");
            }
          }
        }
      }

      function setupMobileNav() {
        window.addEventListener("resize", onResize);
        onResize();
      }

      document.addEventListener("DOMContentLoaded", setupMobileNav);
    </script>
    <script>
      // Copyright 2013 The Chromium Authors. All rights reserved.
      // Use of this source code is governed by a BSD-style license that can be
      // found in the LICENSE file.

      function toggleHelpBox() {
        var helpBoxOuter = document.getElementById("details");
        helpBoxOuter.classList.toggle("hidden");
        var detailsButton = document.getElementById("details-button");
        if (helpBoxOuter.classList.contains("hidden")) detailsButton.innerText = detailsButton.detailsText;
        else detailsButton.innerText = detailsButton.hideDetailsText;

        // Details appears over the main content on small screens.
        if (mobileNav) {
          document.getElementById("main-content").classList.toggle("hidden");
          var runnerContainer = document.querySelector(".runner-container");
          if (runnerContainer) {
            runnerContainer.classList.toggle("hidden");
          }
        }
      }

      function diagnoseErrors() {
        var extensionId = "idddmepepmjcgiedknnmlbadcokidhoa";
        var diagnoseFrame = document.getElementById("diagnose-frame");
        diagnoseFrame.innerHTML = '<iframe src="chrome-extension://' + extensionId + '/index.html"></iframe>';
      }

      // Subframes use a different layout but the same html file.  This is to make it
      // easier to support platforms that load the error page via different
      // mechanisms (Currently just iOS).
      if (window.top.location != window.location) document.documentElement.setAttribute("subframe", "");

      // Re-renders the error page using |strings| as the dictionary of values.
      // Used by NetErrorTabHelper to update DNS error pages with probe results.
      function updateForDnsProbe(strings) {
        var context = new JsEvalContext(strings);
        jstProcess(context, document.getElementById("t"));
      }

      // Given the classList property of an element, adds an icon class to the list
      // and removes the previously-
      function updateIconClass(classList, newClass) {
        var oldClass;

        if (classList.hasOwnProperty("last_icon_class")) {
          oldClass = classList["last_icon_class"];
          if (oldClass == newClass) return;
        }

        classList.add(newClass);
        if (oldClass !== undefined) classList.remove(oldClass);

        classList["last_icon_class"] = newClass;

        new Runner(".interstitial-wrapper");
      }
    </script>
    <script>
      // Copyright (c) 2014 The Chromium Authors. All rights reserved.
      // Use of this source code is governed by a BSD-style license that can be
      // found in the LICENSE file.
      (function () {
        "use strict";
        /**
         * T-Rex runner.
         * @param {string} outerContainerId Outer containing element id.
         * @param {object} opt_config
         * @constructor
         * @export
         */
        function Runner(outerContainerId, opt_config) {
          // Singleton
          if (Runner.instance_) {
            return Runner.instance_;
          }
          Runner.instance_ = this;

          this.outerContainerEl = document.querySelector(outerContainerId);
          this.containerEl = null;
          this.detailsButton = this.outerContainerEl.querySelector("#details-button");

          this.config = opt_config || Runner.config;

          this.dimensions = Runner.defaultDimensions;

          this.canvas = null;
          this.canvasCtx = null;

          this.tRex = null;

          this.distanceMeter = null;
          this.distanceRan = 0;

          this.highestScore = 0;

          this.time = 0;
          this.runningTime = 0;
          this.msPerFrame = 1000 / FPS;
          this.currentSpeed = this.config.SPEED;

          this.obstacles = [];

          this.started = false;
          this.activated = false;
          this.crashed = false;
          this.paused = false;

          this.resizeTimerId_ = null;

          this.playCount = 0;

          // Sound FX.
          this.audioBuffer = null;
          this.soundFx = {};

          // Global web audio context for playing sounds.
          this.audioContext = null;

          // Images.
          this.images = {};
          this.imagesLoaded = 0;
          this.loadImages();
        }
        window["Runner"] = Runner;

        /**
         * Default game width.
         * @const
         */
        var DEFAULT_WIDTH = 600;

        /**
         * Frames per second.
         * @const
         */
        var FPS = 60;

        /** @const */
        var IS_HIDPI = window.devicePixelRatio > 1;

        /** @const */
        var IS_IOS = window.navigator.userAgent.indexOf("UIWebViewForStaticFileContent") > -1;

        /** @const */
        var IS_MOBILE = window.navigator.userAgent.indexOf("Mobi") > -1 || IS_IOS;

        /** @const */
        var IS_TOUCH_ENABLED = "ontouchstart" in window;

        /**
         * Default game configuration.
         * @enum {number}
         */
        Runner.config = {
          ACCELERATION: 0.001,
          BG_CLOUD_SPEED: 0.2,
          BOTTOM_PAD: 10,
          CLEAR_TIME: 3000,
          CLOUD_FREQUENCY: 0.5,
          GAMEOVER_CLEAR_TIME: 750,
          GAP_COEFFICIENT: 0.6,
          GRAVITY: 0.6,
          INITIAL_JUMP_VELOCITY: 12,
          MAX_CLOUDS: 6,
          MAX_OBSTACLE_LENGTH: 3,
          MAX_SPEED: 12,
          MIN_JUMP_HEIGHT: 35,
          MOBILE_SPEED_COEFFICIENT: 1.2,
          RESOURCE_TEMPLATE_ID: "audio-resources",
          SPEED: 6,
          SPEED_DROP_COEFFICIENT: 3,
        };

        /**
         * Default dimensions.
         * @enum {string}
         */
        Runner.defaultDimensions = {
          WIDTH: DEFAULT_WIDTH,
          HEIGHT: 150,
        };

        /**
         * CSS class names.
         * @enum {string}
         */
        Runner.classes = {
          CANVAS: "runner-canvas",
          CONTAINER: "runner-container",
          CRASHED: "crashed",
          ICON: "icon-offline",
          TOUCH_CONTROLLER: "controller",
        };

        /**
         * Image source urls.
         * @enum {array<object>}
         */
        Runner.imageSources = {
          LDPI: [
            { name: "CACTUS_LARGE", id: "1x-obstacle-large" },
            { name: "CACTUS_SMALL", id: "1x-obstacle-small" },
            { name: "CLOUD", id: "1x-cloud" },
            { name: "HORIZON", id: "1x-horizon" },
            { name: "RESTART", id: "1x-restart" },
            { name: "TEXT_SPRITE", id: "1x-text" },
            { name: "TREX", id: "1x-trex" },
          ],
          HDPI: [
            { name: "CACTUS_LARGE", id: "2x-obstacle-large" },
            { name: "CACTUS_SMALL", id: "2x-obstacle-small" },
            { name: "CLOUD", id: "2x-cloud" },
            { name: "HORIZON", id: "2x-horizon" },
            { name: "RESTART", id: "2x-restart" },
            { name: "TEXT_SPRITE", id: "2x-text" },
            { name: "TREX", id: "2x-trex" },
          ],
        };

        /**
         * Sound FX. Reference to the ID of the audio tag on interstitial page.
         * @enum {string}
         */
        Runner.sounds = {
          BUTTON_PRESS: "offline-sound-press",
          HIT: "offline-sound-hit",
          SCORE: "offline-sound-reached",
        };

        /**
         * Key code mapping.
         * @enum {object}
         */
        Runner.keycodes = {
          JUMP: { "38": 1, "32": 1 }, // Up, spacebar
          DUCK: { "40": 1 }, // Down
          RESTART: { "13": 1 }, // Enter
        };

        /**
         * Runner event names.
         * @enum {string}
         */
        Runner.events = {
          ANIM_END: "webkitAnimationEnd",
          CLICK: "click",
          KEYDOWN: "keydown",
          KEYUP: "keyup",
          MOUSEDOWN: "mousedown",
          MOUSEUP: "mouseup",
          RESIZE: "resize",
          TOUCHEND: "touchend",
          TOUCHSTART: "touchstart",
          VISIBILITY: "visibilitychange",
          BLUR: "blur",
          FOCUS: "focus",
          LOAD: "load",
        };

        Runner.prototype = {
          /**
           * Setting individual settings for debugging.
           * @param {string} setting
           * @param {*} value
           */
          updateConfigSetting: function (setting, value) {
            if (setting in this.config && value != undefined) {
              this.config[setting] = value;

              switch (setting) {
                case "GRAVITY":
                case "MIN_JUMP_HEIGHT":
                case "SPEED_DROP_COEFFICIENT":
                  this.tRex.config[setting] = value;
                  break;
                case "INITIAL_JUMP_VELOCITY":
                  this.tRex.setJumpVelocity(value);
                  break;
                case "SPEED":
                  this.setSpeed(value);
                  break;
              }
            }
          },

          /**
           * Load and cache the image assets from the page.
           */
          loadImages: function () {
            var imageSources = IS_HIDPI ? Runner.imageSources.HDPI : Runner.imageSources.LDPI;

            var numImages = imageSources.length;

            for (var i = numImages - 1; i >= 0; i--) {
              var imgSource = imageSources[i];
              this.images[imgSource.name] = document.getElementById(imgSource.id);
            }
            this.init();
          },

          /**
           * Load and decode base 64 encoded sounds.
           */
          loadSounds: function () {
            if (!IS_IOS) {
              this.audioContext = new AudioContext();
              var resourceTemplate = document.getElementById(this.config.RESOURCE_TEMPLATE_ID).content;

              for (var sound in Runner.sounds) {
                var soundSrc = resourceTemplate.getElementById(Runner.sounds[sound]).src;
                soundSrc = soundSrc.substr(soundSrc.indexOf(",") + 1);
                var buffer = decodeBase64ToArrayBuffer(soundSrc);

                // Async, so no guarantee of order in array.
                this.audioContext.decodeAudioData(
                  buffer,
                  function (index, audioData) {
                    this.soundFx[index] = audioData;
                  }.bind(this, sound)
                );
              }
            }
          },

          /**
           * Sets the game speed. Adjust the speed accordingly if on a smaller screen.
           * @param {number} opt_speed
           */
          setSpeed: function (opt_speed) {
            var speed = opt_speed || this.currentSpeed;

            // Reduce the speed on smaller mobile screens.
            if (this.dimensions.WIDTH < DEFAULT_WIDTH) {
              var mobileSpeed = ((speed * this.dimensions.WIDTH) / DEFAULT_WIDTH) * this.config.MOBILE_SPEED_COEFFICIENT;
              this.currentSpeed = mobileSpeed > speed ? speed : mobileSpeed;
            } else if (opt_speed) {
              this.currentSpeed = opt_speed;
            }
          },

          /**
           * Game initialiser.
           */
          init: function () {
            // Hide the static icon.
            document.querySelector("." + Runner.classes.ICON).style.visibility = "hidden";

            this.adjustDimensions();
            this.setSpeed();

            this.containerEl = document.createElement("div");
            this.containerEl.className = Runner.classes.CONTAINER;

            // Player canvas container.
            this.canvas = createCanvas(this.containerEl, this.dimensions.WIDTH, this.dimensions.HEIGHT, Runner.classes.PLAYER);

            this.canvasCtx = this.canvas.getContext("2d");
            this.canvasCtx.fillStyle = "#f7f7f7";
            this.canvasCtx.fill();
            Runner.updateCanvasScaling(this.canvas);

            // Horizon contains clouds, obstacles and the ground.
            this.horizon = new Horizon(this.canvas, this.images, this.dimensions, this.config.GAP_COEFFICIENT);

            // Distance meter
            this.distanceMeter = new DistanceMeter(this.canvas, this.images.TEXT_SPRITE, this.dimensions.WIDTH);

            // Draw t-rex
            this.tRex = new Trex(this.canvas, this.images.TREX);

            this.outerContainerEl.appendChild(this.containerEl);

            if (IS_MOBILE) {
              this.createTouchController();
            }

            this.startListening();
            this.update();

            window.addEventListener(Runner.events.RESIZE, this.debounceResize.bind(this));
          },

          /**
           * Create the touch controller. A div that covers whole screen.
           */
          createTouchController: function () {
            this.touchController = document.createElement("div");
            this.touchController.className = Runner.classes.TOUCH_CONTROLLER;
          },

          /**
           * Debounce the resize event.
           */
          debounceResize: function () {
            if (!this.resizeTimerId_) {
              this.resizeTimerId_ = setInterval(this.adjustDimensions.bind(this), 250);
            }
          },

          /**
           * Adjust game space dimensions on resize.
           */
          adjustDimensions: function () {
            clearInterval(this.resizeTimerId_);
            this.resizeTimerId_ = null;

            var boxStyles = window.getComputedStyle(this.outerContainerEl);
            var padding = Number(boxStyles.paddingLeft.substr(0, boxStyles.paddingLeft.length - 2));

            this.dimensions.WIDTH = this.outerContainerEl.offsetWidth - padding * 2;

            // Redraw the elements back onto the canvas.
            if (this.canvas) {
              this.canvas.width = this.dimensions.WIDTH;
              this.canvas.height = this.dimensions.HEIGHT;

              Runner.updateCanvasScaling(this.canvas);

              this.distanceMeter.calcXPos(this.dimensions.WIDTH);
              this.clearCanvas();
              this.horizon.update(0, 0, true);
              this.tRex.update(0);

              // Outer container and distance meter.
              if (this.activated || this.crashed) {
                this.containerEl.style.width = this.dimensions.WIDTH + "px";
                this.containerEl.style.height = this.dimensions.HEIGHT + "px";
                this.distanceMeter.update(0, Math.ceil(this.distanceRan));
                this.stop();
              } else {
                this.tRex.draw(0, 0);
              }

              // Game over panel.
              if (this.crashed && this.gameOverPanel) {
                this.gameOverPanel.updateDimensions(this.dimensions.WIDTH);
                this.gameOverPanel.draw();
              }
            }
          },

          /**
           * Play the game intro.
           * Canvas container width expands out to the full width.
           */
          playIntro: function () {
            if (!this.started && !this.crashed) {
              this.playingIntro = true;
              this.tRex.playingIntro = true;

              // CSS animation definition.
              var keyframes = "@-webkit-keyframes intro { " + "from { width:" + Trex.config.WIDTH + "px }" + "to { width: " + this.dimensions.WIDTH + "px }" + "}";
              document.styleSheets[0].insertRule(keyframes, 0);

              this.containerEl.addEventListener(Runner.events.ANIM_END, this.startGame.bind(this));

              this.containerEl.style.webkitAnimation = "intro .4s ease-out 1 both";
              this.containerEl.style.width = this.dimensions.WIDTH + "px";

              if (this.touchController) {
                this.outerContainerEl.appendChild(this.touchController);
              }
              this.activated = true;
              this.started = true;
            } else if (this.crashed) {
              this.restart();
            }
          },

          /**
           * Update the game status to started.
           */
          startGame: function () {
            this.runningTime = 0;
            this.playingIntro = false;
            this.tRex.playingIntro = false;
            this.containerEl.style.webkitAnimation = "";
            this.playCount++;

            // Handle tabbing off the page. Pause the current game.
            window.addEventListener(Runner.events.VISIBILITY, this.onVisibilityChange.bind(this));

            window.addEventListener(Runner.events.BLUR, this.onVisibilityChange.bind(this));

            window.addEventListener(Runner.events.FOCUS, this.onVisibilityChange.bind(this));
          },

          clearCanvas: function () {
            this.canvasCtx.clearRect(0, 0, this.dimensions.WIDTH, this.dimensions.HEIGHT);
          },

          /**
           * Update the game frame.
           */
          update: function () {
            this.drawPending = false;

            var now = getTimeStamp();
            var deltaTime = now - (this.time || now);
            this.time = now;

            if (this.activated) {
              this.clearCanvas();

              if (this.tRex.jumping) {
                this.tRex.updateJump(deltaTime, this.config);
              }

              this.runningTime += deltaTime;
              var hasObstacles = this.runningTime > this.config.CLEAR_TIME;

              // First jump triggers the intro.
              if (this.tRex.jumpCount == 1 && !this.playingIntro) {
                this.playIntro();
              }

              // The horizon doesn't move until the intro is over.
              if (this.playingIntro) {
                this.horizon.update(0, this.currentSpeed, hasObstacles);
              } else {
                deltaTime = !this.started ? 0 : deltaTime;
                this.horizon.update(deltaTime, this.currentSpeed, hasObstacles);
              }

              // Check for collisions.
              var collision = hasObstacles && checkForCollision(this.horizon.obstacles[0], this.tRex);

              if (!collision) {
                this.distanceRan += (this.currentSpeed * deltaTime) / this.msPerFrame;

                if (this.currentSpeed < this.config.MAX_SPEED) {
                  this.currentSpeed += this.config.ACCELERATION;
                }
              } else {
                this.gameOver();
              }

              if (this.distanceMeter.getActualDistance(this.distanceRan) > this.distanceMeter.maxScore) {
                this.distanceRan = 0;
              }

              var playAcheivementSound = this.distanceMeter.update(deltaTime, Math.ceil(this.distanceRan));

              if (playAcheivementSound) {
                this.playSound(this.soundFx.SCORE);
              }
            }

            if (!this.crashed) {
              this.tRex.update(deltaTime);
              this.raq();
            }
          },

          /**
           * Event handler.
           */
          handleEvent: function (e) {
            return function (evtType, events) {
              switch (evtType) {
                case events.KEYDOWN:
                case events.TOUCHSTART:
                case events.MOUSEDOWN:
                  this.onKeyDown(e);
                  break;
                case events.KEYUP:
                case events.TOUCHEND:
                case events.MOUSEUP:
                  this.onKeyUp(e);
                  break;
              }
            }.bind(this)(e.type, Runner.events);
          },

          /**
           * Bind relevant key / mouse / touch listeners.
           */
          startListening: function () {
            // Keys.
            document.addEventListener(Runner.events.KEYDOWN, this);
            document.addEventListener(Runner.events.KEYUP, this);

            if (IS_MOBILE) {
              // Mobile only touch devices.
              this.touchController.addEventListener(Runner.events.TOUCHSTART, this);
              this.touchController.addEventListener(Runner.events.TOUCHEND, this);
              this.containerEl.addEventListener(Runner.events.TOUCHSTART, this);
            } else {
              // Mouse.
              document.addEventListener(Runner.events.MOUSEDOWN, this);
              document.addEventListener(Runner.events.MOUSEUP, this);
            }
          },

          /**
           * Remove all listeners.
           */
          stopListening: function () {
            document.removeEventListener(Runner.events.KEYDOWN, this);
            document.removeEventListener(Runner.events.KEYUP, this);

            if (IS_MOBILE) {
              this.touchController.removeEventListener(Runner.events.TOUCHSTART, this);
              this.touchController.removeEventListener(Runner.events.TOUCHEND, this);
              this.containerEl.removeEventListener(Runner.events.TOUCHSTART, this);
            } else {
              document.removeEventListener(Runner.events.MOUSEDOWN, this);
              document.removeEventListener(Runner.events.MOUSEUP, this);
            }
          },

          /**
           * Process keydown.
           * @param {Event} e
           */
          onKeyDown: function (e) {
            if (e.target != this.detailsButton) {
              if (!this.crashed && (Runner.keycodes.JUMP[String(e.keyCode)] || e.type == Runner.events.TOUCHSTART)) {
                if (!this.activated) {
                  this.loadSounds();
                  this.activated = true;
                }

                if (!this.tRex.jumping) {
                  this.playSound(this.soundFx.BUTTON_PRESS);
                  this.tRex.startJump();
                }
              }

              if (this.crashed && e.type == Runner.events.TOUCHSTART && e.currentTarget == this.containerEl) {
                this.restart();
              }
            }

            // Speed drop, activated only when jump key is not pressed.
            if (Runner.keycodes.DUCK[e.keyCode] && this.tRex.jumping) {
              e.preventDefault();
              this.tRex.setSpeedDrop();
            }
          },

          /**
           * Process key up.
           * @param {Event} e
           */
          onKeyUp: function (e) {
            var keyCode = String(e.keyCode);
            var isjumpKey = Runner.keycodes.JUMP[keyCode] || e.type == Runner.events.TOUCHEND || e.type == Runner.events.MOUSEDOWN;

            if (this.isRunning() && isjumpKey) {
              this.tRex.endJump();
            } else if (Runner.keycodes.DUCK[keyCode]) {
              this.tRex.speedDrop = false;
            } else if (this.crashed) {
              // Check that enough time has elapsed before allowing jump key to restart.
              var deltaTime = getTimeStamp() - this.time;

              if (Runner.keycodes.RESTART[keyCode] || (e.type == Runner.events.MOUSEUP && e.target == this.canvas) || (deltaTime >= this.config.GAMEOVER_CLEAR_TIME && Runner.keycodes.JUMP[keyCode])) {
                this.restart();
              }
            } else if (this.paused && isjumpKey) {
              this.play();
            }
          },

          /**
           * RequestAnimationFrame wrapper.
           */
          raq: function () {
            if (!this.drawPending) {
              this.drawPending = true;
              this.raqId = requestAnimationFrame(this.update.bind(this));
            }
          },

          /**
           * Whether the game is running.
           * @return {boolean}
           */
          isRunning: function () {
            return !!this.raqId;
          },

          /**
           * Game over state.
           */
          gameOver: function () {
            this.playSound(this.soundFx.HIT);
            vibrate(200);

            this.stop();
            this.crashed = true;
            this.distanceMeter.acheivement = false;

            this.tRex.update(100, Trex.status.CRASHED);

            // Game over panel.
            if (!this.gameOverPanel) {
              this.gameOverPanel = new GameOverPanel(this.canvas, this.images.TEXT_SPRITE, this.images.RESTART, this.dimensions);
            } else {
              this.gameOverPanel.draw();
            }

            // Update the high score.
            if (this.distanceRan > this.highestScore) {
              this.highestScore = Math.ceil(this.distanceRan);
              this.distanceMeter.setHighScore(this.highestScore);
            }

            // Reset the time clock.
            this.time = getTimeStamp();
          },

          stop: function () {
            this.activated = false;
            this.paused = true;
            cancelAnimationFrame(this.raqId);
            this.raqId = 0;
          },

          play: function () {
            if (!this.crashed) {
              this.activated = true;
              this.paused = false;
              this.tRex.update(0, Trex.status.RUNNING);
              this.time = getTimeStamp();
              this.update();
            }
          },

          restart: function () {
            if (!this.raqId) {
              this.playCount++;
              this.runningTime = 0;
              this.activated = true;
              this.crashed = false;
              this.distanceRan = 0;
              this.setSpeed(this.config.SPEED);

              this.time = getTimeStamp();
              this.containerEl.classList.remove(Runner.classes.CRASHED);
              this.clearCanvas();
              this.distanceMeter.reset(this.highestScore);
              this.horizon.reset();
              this.tRex.reset();
              this.playSound(this.soundFx.BUTTON_PRESS);

              this.update();
            }
          },

          /**
           * Pause the game if the tab is not in focus.
           */
          onVisibilityChange: function (e) {
            if (document.hidden || document.webkitHidden || e.type == "blur") {
              this.stop();
            } else {
              this.play();
            }
          },

          /**
           * Play a sound.
           * @param {SoundBuffer} soundBuffer
           */
          playSound: function (soundBuffer) {
            if (soundBuffer) {
              var sourceNode = this.audioContext.createBufferSource();
              sourceNode.buffer = soundBuffer;
              sourceNode.connect(this.audioContext.destination);
              sourceNode.start(0);
            }
          },
        };

        /**
         * Updates the canvas size taking into
         * account the backing store pixel ratio and
         * the device pixel ratio.
         *
         * See article by Paul Lewis:
         * http://www.html5rocks.com/en/tutorials/canvas/hidpi/
         *
         * @param {HTMLCanvasElement} canvas
         * @param {number} opt_width
         * @param {number} opt_height
         * @return {boolean} Whether the canvas was scaled.
         */
        Runner.updateCanvasScaling = function (canvas, opt_width, opt_height) {
          var context = canvas.getContext("2d");

          // Query the various pixel ratios
          var devicePixelRatio = Math.floor(window.devicePixelRatio) || 1;
          var backingStoreRatio = Math.floor(context.webkitBackingStorePixelRatio) || 1;
          var ratio = devicePixelRatio / backingStoreRatio;

          // Upscale the canvas if the two ratios don't match
          if (devicePixelRatio !== backingStoreRatio) {
            var oldWidth = opt_width || canvas.width;
            var oldHeight = opt_height || canvas.height;

            canvas.width = oldWidth * ratio;
            canvas.height = oldHeight * ratio;

            canvas.style.width = oldWidth + "px";
            canvas.style.height = oldHeight + "px";

            // Scale the context to counter the fact that we've manually scaled
            // our canvas element.
            context.scale(ratio, ratio);
            return true;
          } else if (devicePixelRatio == 1) {
            // Reset the canvas width / height. Fixes scaling bug when the page is
            // zoomed and the devicePixelRatio changes accordingly.
            canvas.style.width = canvas.width + "px";
            canvas.style.height = canvas.height + "px";
          }
          return false;
        };

        /**
         * Get random number.
         * @param {number} min
         * @param {number} max
         * @param {number}
         */
        function getRandomNum(min, max) {
          return Math.floor(Math.random() * (max - min + 1)) + min;
        }

        /**
         * Vibrate on mobile devices.
         * @param {number} duration Duration of the vibration in milliseconds.
         */
        function vibrate(duration) {
          if (IS_MOBILE && window.navigator.vibrate) {
            window.navigator.vibrate(duration);
          }
        }

        /**
         * Create canvas element.
         * @param {HTMLElement} container Element to append canvas to.
         * @param {number} width
         * @param {number} height
         * @param {string} opt_classname
         * @return {HTMLCanvasElement}
         */
        function createCanvas(container, width, height, opt_classname) {
          var canvas = document.createElement("canvas");
          canvas.className = opt_classname ? Runner.classes.CANVAS + " " + opt_classname : Runner.classes.CANVAS;
          canvas.width = width;
          canvas.height = height;
          container.appendChild(canvas);

          return canvas;
        }

        /**
         * Decodes the base 64 audio to ArrayBuffer used by Web Audio.
         * @param {string} base64String
         */
        function decodeBase64ToArrayBuffer(base64String) {
          var len = (base64String.length / 4) * 3;
          var str = atob(base64String);
          var arrayBuffer = new ArrayBuffer(len);
          var bytes = new Uint8Array(arrayBuffer);

          for (var i = 0; i < len; i++) {
            bytes[i] = str.charCodeAt(i);
          }
          return bytes.buffer;
        }

        /**
         * Return the current timestamp.
         * @return {number}
         */
        function getTimeStamp() {
          return IS_IOS ? new Date().getTime() : performance.now();
        }

        //******************************************************************************

        /**
         * Game over panel.
         * @param {!HTMLCanvasElement} canvas
         * @param {!HTMLImage} textSprite
         * @param {!HTMLImage} restartImg
         * @param {!Object} dimensions Canvas dimensions.
         * @constructor
         */
        function GameOverPanel(canvas, textSprite, restartImg, dimensions) {
          this.canvas = canvas;
          this.canvasCtx = canvas.getContext("2d");
          this.canvasDimensions = dimensions;
          this.textSprite = textSprite;
          this.restartImg = restartImg;
          this.draw();
        }

        /**
         * Dimensions used in the panel.
         * @enum {number}
         */
        GameOverPanel.dimensions = {
          TEXT_X: 0,
          TEXT_Y: 13,
          TEXT_WIDTH: 191,
          TEXT_HEIGHT: 11,
          RESTART_WIDTH: 36,
          RESTART_HEIGHT: 32,
        };

        GameOverPanel.prototype = {
          /**
           * Update the panel dimensions.
           * @param {number} width New canvas width.
           * @param {number} opt_height Optional new canvas height.
           */
          updateDimensions: function (width, opt_height) {
            this.canvasDimensions.WIDTH = width;
            if (opt_height) {
              this.canvasDimensions.HEIGHT = opt_height;
            }
          },

          /**
           * Draw the panel.
           */
          draw: function () {
            var dimensions = GameOverPanel.dimensions;

            var centerX = this.canvasDimensions.WIDTH / 2;

            // Game over text.
            var textSourceX = dimensions.TEXT_X;
            var textSourceY = dimensions.TEXT_Y;
            var textSourceWidth = dimensions.TEXT_WIDTH;
            var textSourceHeight = dimensions.TEXT_HEIGHT;

            var textTargetX = Math.round(centerX - dimensions.TEXT_WIDTH / 2);
            var textTargetY = Math.round((this.canvasDimensions.HEIGHT - 25) / 3);
            var textTargetWidth = dimensions.TEXT_WIDTH;
            var textTargetHeight = dimensions.TEXT_HEIGHT;

            var restartSourceWidth = dimensions.RESTART_WIDTH;
            var restartSourceHeight = dimensions.RESTART_HEIGHT;
            var restartTargetX = centerX - dimensions.RESTART_WIDTH / 2;
            var restartTargetY = this.canvasDimensions.HEIGHT / 2;

            if (IS_HIDPI) {
              textSourceY *= 2;
              textSourceX *= 2;
              textSourceWidth *= 2;
              textSourceHeight *= 2;
              restartSourceWidth *= 2;
              restartSourceHeight *= 2;
            }

            // Game over text from sprite.
            this.canvasCtx.drawImage(this.textSprite, textSourceX, textSourceY, textSourceWidth, textSourceHeight, textTargetX, textTargetY, textTargetWidth, textTargetHeight);

            // Restart button.
            this.canvasCtx.drawImage(this.restartImg, 0, 0, restartSourceWidth, restartSourceHeight, restartTargetX, restartTargetY, dimensions.RESTART_WIDTH, dimensions.RESTART_HEIGHT);
          },
        };

        //******************************************************************************

        /**
         * Check for a collision.
         * @param {!Obstacle} obstacle
         * @param {!Trex} tRex T-rex object.
         * @param {HTMLCanvasContext} opt_canvasCtx Optional canvas context for drawing
         *    collision boxes.
         * @return {Array<CollisionBox>}
         */
        function checkForCollision(obstacle, tRex, opt_canvasCtx) {
          var obstacleBoxXPos = Runner.defaultDimensions.WIDTH + obstacle.xPos;

          // Adjustments are made to the bounding box as there is a 1 pixel white
          // border around the t-rex and obstacles.
          var tRexBox = new CollisionBox(tRex.xPos + 1, tRex.yPos + 1, tRex.config.WIDTH - 2, tRex.config.HEIGHT - 2);

          var obstacleBox = new CollisionBox(obstacle.xPos + 1, obstacle.yPos + 1, obstacle.typeConfig.width * obstacle.size - 2, obstacle.typeConfig.height - 2);

          // Debug outer box
          if (opt_canvasCtx) {
            drawCollisionBoxes(opt_canvasCtx, tRexBox, obstacleBox);
          }

          // Simple outer bounds check.
          if (boxCompare(tRexBox, obstacleBox)) {
            var collisionBoxes = obstacle.collisionBoxes;
            var tRexCollisionBoxes = Trex.collisionBoxes;

            // Detailed axis aligned box check.
            for (var t = 0; t < tRexCollisionBoxes.length; t++) {
              for (var i = 0; i < collisionBoxes.length; i++) {
                // Adjust the box to actual positions.
                var adjTrexBox = createAdjustedCollisionBox(tRexCollisionBoxes[t], tRexBox);
                var adjObstacleBox = createAdjustedCollisionBox(collisionBoxes[i], obstacleBox);
                var crashed = boxCompare(adjTrexBox, adjObstacleBox);

                // Draw boxes for debug.
                if (opt_canvasCtx) {
                  drawCollisionBoxes(opt_canvasCtx, adjTrexBox, adjObstacleBox);
                }

                if (crashed) {
                  return [adjTrexBox, adjObstacleBox];
                }
              }
            }
          }
          return false;
        }

        /**
         * Adjust the collision box.
         * @param {!CollisionBox} box The original box.
         * @param {!CollisionBox} adjustment Adjustment box.
         * @return {CollisionBox} The adjusted collision box object.
         */
        function createAdjustedCollisionBox(box, adjustment) {
          return new CollisionBox(box.x + adjustment.x, box.y + adjustment.y, box.width, box.height);
        }

        /**
         * Draw the collision boxes for debug.
         */
        function drawCollisionBoxes(canvasCtx, tRexBox, obstacleBox) {
          canvasCtx.save();
          canvasCtx.strokeStyle = "#f00";
          canvasCtx.strokeRect(tRexBox.x, tRexBox.y, tRexBox.width, tRexBox.height);

          canvasCtx.strokeStyle = "#0f0";
          canvasCtx.strokeRect(obstacleBox.x, obstacleBox.y, obstacleBox.width, obstacleBox.height);
          canvasCtx.restore();
        }

        /**
         * Compare two collision boxes for a collision.
         * @param {CollisionBox} tRexBox
         * @param {CollisionBox} obstacleBox
         * @return {boolean} Whether the boxes intersected.
         */
        function boxCompare(tRexBox, obstacleBox) {
          var crashed = false;
          var tRexBoxX = tRexBox.x;
          var tRexBoxY = tRexBox.y;

          var obstacleBoxX = obstacleBox.x;
          var obstacleBoxY = obstacleBox.y;

          // Axis-Aligned Bounding Box method.
          if (tRexBox.x < obstacleBoxX + obstacleBox.width && tRexBox.x + tRexBox.width > obstacleBoxX && tRexBox.y < obstacleBox.y + obstacleBox.height && tRexBox.height + tRexBox.y > obstacleBox.y) {
            crashed = true;
          }

          return crashed;
        }

        //******************************************************************************

        /**
         * Collision box object.
         * @param {number} x X position.
         * @param {number} y Y Position.
         * @param {number} w Width.
         * @param {number} h Height.
         */
        function CollisionBox(x, y, w, h) {
          this.x = x;
          this.y = y;
          this.width = w;
          this.height = h;
        }

        //******************************************************************************

        /**
         * Obstacle.
         * @param {HTMLCanvasCtx} canvasCtx
         * @param {Obstacle.type} type
         * @param {image} obstacleImg Image sprite.
         * @param {Object} dimensions
         * @param {number} gapCoefficient Mutipler in determining the gap.
         * @param {number} speed
         */
        function Obstacle(canvasCtx, type, obstacleImg, dimensions, gapCoefficient, speed) {
          this.canvasCtx = canvasCtx;
          this.image = obstacleImg;
          this.typeConfig = type;
          this.gapCoefficient = gapCoefficient;
          this.size = getRandomNum(1, Obstacle.MAX_OBSTACLE_LENGTH);
          this.dimensions = dimensions;
          this.remove = false;
          this.xPos = 0;
          this.yPos = this.typeConfig.yPos;
          this.width = 0;
          this.collisionBoxes = [];
          this.gap = 0;

          this.init(speed);
        }

        /**
         * Coefficient for calculating the maximum gap.
         * @const
         */
        Obstacle.MAX_GAP_COEFFICIENT = 1.5;

        /**
         * Maximum obstacle grouping count.
         * @const
         */
        (Obstacle.MAX_OBSTACLE_LENGTH = 3),
          (Obstacle.prototype = {
            /**
             * Initialise the DOM for the obstacle.
             * @param {number} speed
             */
            init: function (speed) {
              this.cloneCollisionBoxes();

              // Only allow sizing if we're at the right speed.
              if (this.size > 1 && this.typeConfig.multipleSpeed > speed) {
                this.size = 1;
              }

              this.width = this.typeConfig.width * this.size;
              this.xPos = this.dimensions.WIDTH - this.width;

              this.draw();

              // Make collision box adjustments,
              // Central box is adjusted to the size as one box.
              //      ____        ______        ________
              //    _|   |-|    _|     |-|    _|       |-|
              //   | |<->| |   | |<--->| |   | |<----->| |
              //   | | 1 | |   | |  2  | |   | |   3   | |
              //   |_|___|_|   |_|_____|_|   |_|_______|_|
              //
              if (this.size > 1) {
                this.collisionBoxes[1].width = this.width - this.collisionBoxes[0].width - this.collisionBoxes[2].width;
                this.collisionBoxes[2].x = this.width - this.collisionBoxes[2].width;
              }

              this.gap = this.getGap(this.gapCoefficient, speed);
            },

            /**
             * Draw and crop based on size.
             */
            draw: function () {
              var sourceWidth = this.typeConfig.width;
              var sourceHeight = this.typeConfig.height;

              if (IS_HIDPI) {
                sourceWidth = sourceWidth * 2;
                sourceHeight = sourceHeight * 2;
              }

              // Sprite
              var sourceX = sourceWidth * this.size * (0.5 * (this.size - 1));
              this.canvasCtx.drawImage(this.image, sourceX, 0, sourceWidth * this.size, sourceHeight, this.xPos, this.yPos, this.typeConfig.width * this.size, this.typeConfig.height);
            },

            /**
             * Obstacle frame update.
             * @param {number} deltaTime
             * @param {number} speed
             */
            update: function (deltaTime, speed) {
              if (!this.remove) {
                this.xPos -= Math.floor(((speed * FPS) / 1000) * deltaTime);
                this.draw();

                if (!this.isVisible()) {
                  this.remove = true;
                }
              }
            },

            /**
             * Calculate a random gap size.
             * - Minimum gap gets wider as speed increses
             * @param {number} gapCoefficient
             * @param {number} speed
             * @return {number} The gap size.
             */
            getGap: function (gapCoefficient, speed) {
              var minGap = Math.round(this.width * speed + this.typeConfig.minGap * gapCoefficient);
              var maxGap = Math.round(minGap * Obstacle.MAX_GAP_COEFFICIENT);
              return getRandomNum(minGap, maxGap);
            },

            /**
             * Check if obstacle is visible.
             * @return {boolean} Whether the obstacle is in the game area.
             */
            isVisible: function () {
              return this.xPos + this.width > 0;
            },

            /**
             * Make a copy of the collision boxes, since these will change based on
             * obstacle type and size.
             */
            cloneCollisionBoxes: function () {
              var collisionBoxes = this.typeConfig.collisionBoxes;

              for (var i = collisionBoxes.length - 1; i >= 0; i--) {
                this.collisionBoxes[i] = new CollisionBox(collisionBoxes[i].x, collisionBoxes[i].y, collisionBoxes[i].width, collisionBoxes[i].height);
              }
            },
          });

        /**
         * Obstacle definitions.
         * minGap: minimum pixel space betweeen obstacles.
         * multipleSpeed: Speed at which multiples are allowed.
         */
        Obstacle.types = [
          {
            type: "CACTUS_SMALL",
            className: " cactus cactus-small ",
            width: 17,
            height: 35,
            yPos: 105,
            multipleSpeed: 3,
            minGap: 120,
            collisionBoxes: [new CollisionBox(0, 7, 5, 27), new CollisionBox(4, 0, 6, 34), new CollisionBox(10, 4, 7, 14)],
          },
          {
            type: "CACTUS_LARGE",
            className: " cactus cactus-large ",
            width: 25,
            height: 50,
            yPos: 90,
            multipleSpeed: 6,
            minGap: 120,
            collisionBoxes: [new CollisionBox(0, 12, 7, 38), new CollisionBox(8, 0, 7, 49), new CollisionBox(13, 10, 10, 38)],
          },
        ];

        //******************************************************************************
        /**
         * T-rex game character.
         * @param {HTMLCanvas} canvas
         * @param {HTMLImage} image Character image.
         * @constructor
         */
        function Trex(canvas, image) {
          this.canvas = canvas;
          this.canvasCtx = canvas.getContext("2d");
          this.image = image;
          this.xPos = 0;
          this.yPos = 0;
          // Position when on the ground.
          this.groundYPos = 0;
          this.currentFrame = 0;
          this.currentAnimFrames = [];
          this.blinkDelay = 0;
          this.animStartTime = 0;
          this.timer = 0;
          this.msPerFrame = 1000 / FPS;
          this.config = Trex.config;
          // Current status.
          this.status = Trex.status.WAITING;

          this.jumping = false;
          this.jumpVelocity = 0;
          this.reachedMinHeight = false;
          this.speedDrop = false;
          this.jumpCount = 0;
          this.jumpspotX = 0;

          this.init();
        }

        /**
         * T-rex player config.
         * @enum {number}
         */
        Trex.config = {
          DROP_VELOCITY: -5,
          GRAVITY: 0.6,
          HEIGHT: 47,
          INIITAL_JUMP_VELOCITY: -10,
          INTRO_DURATION: 1500,
          MAX_JUMP_HEIGHT: 30,
          MIN_JUMP_HEIGHT: 30,
          SPEED_DROP_COEFFICIENT: 3,
          SPRITE_WIDTH: 262,
          START_X_POS: 50,
          WIDTH: 44,
        };

        /**
         * Used in collision detection.
         * @type {Array<CollisionBox>}
         */
        Trex.collisionBoxes = [new CollisionBox(1, -1, 30, 26), new CollisionBox(32, 0, 8, 16), new CollisionBox(10, 35, 14, 8), new CollisionBox(1, 24, 29, 5), new CollisionBox(5, 30, 21, 4), new CollisionBox(9, 34, 15, 4)];

        /**
         * Animation states.
         * @enum {string}
         */
        Trex.status = {
          CRASHED: "CRASHED",
          JUMPING: "JUMPING",
          RUNNING: "RUNNING",
          WAITING: "WAITING",
        };

        /**
         * Blinking coefficient.
         * @const
         */
        Trex.BLINK_TIMING = 7000;

        /**
         * Animation config for different states.
         * @enum {object}
         */
        Trex.animFrames = {
          WAITING: {
            frames: [44, 0],
            msPerFrame: 1000 / 3,
          },
          RUNNING: {
            frames: [88, 132],
            msPerFrame: 1000 / 12,
          },
          CRASHED: {
            frames: [220],
            msPerFrame: 1000 / 60,
          },
          JUMPING: {
            frames: [0],
            msPerFrame: 1000 / 60,
          },
        };

        Trex.prototype = {
          /**
           * T-rex player initaliser.
           * Sets the t-rex to blink at random intervals.
           */
          init: function () {
            this.blinkDelay = this.setBlinkDelay();
            this.groundYPos = Runner.defaultDimensions.HEIGHT - this.config.HEIGHT - Runner.config.BOTTOM_PAD;
            this.yPos = this.groundYPos;
            this.minJumpHeight = this.groundYPos - this.config.MIN_JUMP_HEIGHT;

            this.draw(0, 0);
            this.update(0, Trex.status.WAITING);
          },

          /**
           * Setter for the jump velocity.
           * The approriate drop velocity is also set.
           */
          setJumpVelocity: function (setting) {
            this.config.INIITAL_JUMP_VELOCITY = -setting;
            this.config.DROP_VELOCITY = -setting / 2;
          },

          /**
           * Set the animation status.
           * @param {!number} deltaTime
           * @param {Trex.status} status Optional status to switch to.
           */
          update: function (deltaTime, opt_status) {
            this.timer += deltaTime;

            // Update the status.
            if (opt_status) {
              this.status = opt_status;
              this.currentFrame = 0;
              this.msPerFrame = Trex.animFrames[opt_status].msPerFrame;
              this.currentAnimFrames = Trex.animFrames[opt_status].frames;

              if (opt_status == Trex.status.WAITING) {
                this.animStartTime = getTimeStamp();
                this.setBlinkDelay();
              }
            }

            // Game intro animation, T-rex moves in from the left.
            if (this.playingIntro && this.xPos < this.config.START_X_POS) {
              this.xPos += Math.round((this.config.START_X_POS / this.config.INTRO_DURATION) * deltaTime);
            }

            if (this.status == Trex.status.WAITING) {
              this.blink(getTimeStamp());
            } else {
              this.draw(this.currentAnimFrames[this.currentFrame], 0);
            }

            // Update the frame position.
            if (this.timer >= this.msPerFrame) {
              this.currentFrame = this.currentFrame == this.currentAnimFrames.length - 1 ? 0 : this.currentFrame + 1;
              this.timer = 0;
            }
          },

          /**
           * Draw the t-rex to a particular position.
           * @param {number} x
           * @param {number} y
           */
          draw: function (x, y) {
            var sourceX = x;
            var sourceY = y;
            var sourceWidth = this.config.WIDTH;
            var sourceHeight = this.config.HEIGHT;

            if (IS_HIDPI) {
              sourceX *= 2;
              sourceY *= 2;
              sourceWidth *= 2;
              sourceHeight *= 2;
            }

            this.canvasCtx.drawImage(this.image, sourceX, sourceY, sourceWidth, sourceHeight, this.xPos, this.yPos, this.config.WIDTH, this.config.HEIGHT);
          },

          /**
           * Sets a random time for the blink to happen.
           */
          setBlinkDelay: function () {
            this.blinkDelay = Math.ceil(Math.random() * Trex.BLINK_TIMING);
          },

          /**
           * Make t-rex blink at random intervals.
           * @param {number} time Current time in milliseconds.
           */
          blink: function (time) {
            var deltaTime = time - this.animStartTime;

            if (deltaTime >= this.blinkDelay) {
              this.draw(this.currentAnimFrames[this.currentFrame], 0);

              if (this.currentFrame == 1) {
                // Set new random delay to blink.
                this.setBlinkDelay();
                this.animStartTime = time;
              }
            }
          },

          /**
           * Initialise a jump.
           */
          startJump: function () {
            if (!this.jumping) {
              this.update(0, Trex.status.JUMPING);
              this.jumpVelocity = this.config.INIITAL_JUMP_VELOCITY;
              this.jumping = true;
              this.reachedMinHeight = false;
              this.speedDrop = false;
            }
          },

          /**
           * Jump is complete, falling down.
           */
          endJump: function () {
            if (this.reachedMinHeight && this.jumpVelocity < this.config.DROP_VELOCITY) {
              this.jumpVelocity = this.config.DROP_VELOCITY;
            }
          },

          /**
           * Update frame for a jump.
           * @param {number} deltaTime
           */
          updateJump: function (deltaTime) {
            var msPerFrame = Trex.animFrames[this.status].msPerFrame;
            var framesElapsed = deltaTime / msPerFrame;

            // Speed drop makes Trex fall faster.
            if (this.speedDrop) {
              this.yPos += Math.round(this.jumpVelocity * this.config.SPEED_DROP_COEFFICIENT * framesElapsed);
            } else {
              this.yPos += Math.round(this.jumpVelocity * framesElapsed);
            }

            this.jumpVelocity += this.config.GRAVITY * framesElapsed;

            // Minimum height has been reached.
            if (this.yPos < this.minJumpHeight || this.speedDrop) {
              this.reachedMinHeight = true;
            }

            // Reached max height
            if (this.yPos < this.config.MAX_JUMP_HEIGHT || this.speedDrop) {
              this.endJump();
            }

            // Back down at ground level. Jump completed.
            if (this.yPos > this.groundYPos) {
              this.reset();
              this.jumpCount++;
            }

            this.update(deltaTime);
          },

          /**
           * Set the speed drop. Immediately cancels the current jump.
           */
          setSpeedDrop: function () {
            this.speedDrop = true;
            this.jumpVelocity = 1;
          },

          /**
           * Reset the t-rex to running at start of game.
           */
          reset: function () {
            this.yPos = this.groundYPos;
            this.jumpVelocity = 0;
            this.jumping = false;
            this.update(0, Trex.status.RUNNING);
            this.midair = false;
            this.speedDrop = false;
            this.jumpCount = 0;
          },
        };

        //******************************************************************************

        /**
         * Handles displaying the distance meter.
         * @param {!HTMLCanvasElement} canvas
         * @param {!HTMLImage} spriteSheet Image sprite.
         * @param {number} canvasWidth
         * @constructor
         */
        function DistanceMeter(canvas, spriteSheet, canvasWidth) {
          this.canvas = canvas;
          this.canvasCtx = canvas.getContext("2d");
          this.image = spriteSheet;
          this.x = 0;
          this.y = 5;

          this.currentDistance = 0;
          this.maxScore = 0;
          this.highScore = 0;
          this.container = null;

          this.digits = [];
          this.acheivement = false;
          this.defaultString = "";
          this.flashTimer = 0;
          this.flashIterations = 0;

          this.config = DistanceMeter.config;
          this.init(canvasWidth);
        }

        /**
         * @enum {number}
         */
        DistanceMeter.dimensions = {
          WIDTH: 10,
          HEIGHT: 13,
          DEST_WIDTH: 11,
        };

        /**
         * Y positioning of the digits in the sprite sheet.
         * X position is always 0.
         * @type {array<number>}
         */
        DistanceMeter.yPos = [0, 13, 27, 40, 53, 67, 80, 93, 107, 120];

        /**
         * Distance meter config.
         * @enum {number}
         */
        DistanceMeter.config = {
          // Number of digits.
          MAX_DISTANCE_UNITS: 5,

          // Distance that causes achievement animation.
          ACHIEVEMENT_DISTANCE: 100,

          // Used for conversion from pixel distance to a scaled unit.
          COEFFICIENT: 0.025,

          // Flash duration in milliseconds.
          FLASH_DURATION: 1000 / 4,

          // Flash iterations for achievement animation.
          FLASH_ITERATIONS: 3,
        };

        DistanceMeter.prototype = {
          /**
           * Initialise the distance meter to '00000'.
           * @param {number} width Canvas width in px.
           */
          init: function (width) {
            var maxDistanceStr = "";

            this.calcXPos(width);
            this.maxScore = this.config.MAX_DISTANCE_UNITS;
            for (var i = 0; i < this.config.MAX_DISTANCE_UNITS; i++) {
              this.draw(i, 0);
              this.defaultString += "0";
              maxDistanceStr += "9";
            }

            this.maxScore = parseInt(maxDistanceStr);
          },

          /**
           * Calculate the xPos in the canvas.
           * @param {number} canvasWidth
           */
          calcXPos: function (canvasWidth) {
            this.x = canvasWidth - DistanceMeter.dimensions.DEST_WIDTH * (this.config.MAX_DISTANCE_UNITS + 1);
          },

          /**
           * Draw a digit to canvas.
           * @param {number} digitPos Position of the digit.
           * @param {number} value Digit value 0-9.
           * @param {boolean} opt_highScore Whether drawing the high score.
           */
          draw: function (digitPos, value, opt_highScore) {
            var sourceWidth = DistanceMeter.dimensions.WIDTH;
            var sourceHeight = DistanceMeter.dimensions.HEIGHT;
            var sourceX = DistanceMeter.dimensions.WIDTH * value;

            var targetX = digitPos * DistanceMeter.dimensions.DEST_WIDTH;
            var targetY = this.y;
            var targetWidth = DistanceMeter.dimensions.WIDTH;
            var targetHeight = DistanceMeter.dimensions.HEIGHT;

            // For high DPI we 2x source values.
            if (IS_HIDPI) {
              sourceWidth *= 2;
              sourceHeight *= 2;
              sourceX *= 2;
            }

            this.canvasCtx.save();

            if (opt_highScore) {
              // Left of the current score.
              var highScoreX = this.x - this.config.MAX_DISTANCE_UNITS * 2 * DistanceMeter.dimensions.WIDTH;
              this.canvasCtx.translate(highScoreX, this.y);
            } else {
              this.canvasCtx.translate(this.x, this.y);
            }

            this.canvasCtx.drawImage(this.image, sourceX, 0, sourceWidth, sourceHeight, targetX, targetY, targetWidth, targetHeight);

            this.canvasCtx.restore();
          },

          /**
           * Covert pixel distance to a 'real' distance.
           * @param {number} distance Pixel distance ran.
           * @return {number} The 'real' distance ran.
           */
          getActualDistance: function (distance) {
            return distance ? Math.round(distance * this.config.COEFFICIENT) : 0;
          },

          /**
           * Update the distance meter.
           * @param {number} deltaTime
           * @param {number} distance
           * @return {boolean} Whether the acheivement sound fx should be played.
           */
          update: function (deltaTime, distance) {
            var paint = true;
            var playSound = false;

            if (!this.acheivement) {
              distance = this.getActualDistance(distance);

              if (distance > 0) {
                // Acheivement unlocked
                if (distance % this.config.ACHIEVEMENT_DISTANCE == 0) {
                  // Flash score and play sound.
                  this.acheivement = true;
                  this.flashTimer = 0;
                  playSound = true;
                }

                // Create a string representation of the distance with leading 0.
                var distanceStr = (this.defaultString + distance).substr(-this.config.MAX_DISTANCE_UNITS);
                this.digits = distanceStr.split("");
              } else {
                this.digits = this.defaultString.split("");
              }
            } else {
              // Control flashing of the score on reaching acheivement.
              if (this.flashIterations <= this.config.FLASH_ITERATIONS) {
                this.flashTimer += deltaTime;

                if (this.flashTimer < this.config.FLASH_DURATION) {
                  paint = false;
                } else if (this.flashTimer > this.config.FLASH_DURATION * 2) {
                  this.flashTimer = 0;
                  this.flashIterations++;
                }
              } else {
                this.acheivement = false;
                this.flashIterations = 0;
                this.flashTimer = 0;
              }
            }

            // Draw the digits if not flashing.
            if (paint) {
              for (var i = this.digits.length - 1; i >= 0; i--) {
                this.draw(i, parseInt(this.digits[i]));
              }
            }

            this.drawHighScore();

            return playSound;
          },

          /**
           * Draw the high score.
           */
          drawHighScore: function () {
            this.canvasCtx.save();
            this.canvasCtx.globalAlpha = 0.8;
            for (var i = this.highScore.length - 1; i >= 0; i--) {
              this.draw(i, parseInt(this.highScore[i], 10), true);
            }
            this.canvasCtx.restore();
          },

          /**
           * Set the highscore as a array string.
           * Position of char in the sprite: H - 10, I - 11.
           * @param {number} distance Distance ran in pixels.
           */
          setHighScore: function (distance) {
            distance = this.getActualDistance(distance);
            var highScoreStr = (this.defaultString + distance).substr(-this.config.MAX_DISTANCE_UNITS);

            this.highScore = ["10", "11", ""].concat(highScoreStr.split(""));
          },

          /**
           * Reset the distance meter back to '00000'.
           */
          reset: function () {
            this.update(0);
            this.acheivement = false;
          },
        };

        //******************************************************************************

        /**
         * Cloud background item.
         * Similar to an obstacle object but without collision boxes.
         * @param {HTMLCanvasElement} canvas Canvas element.
         * @param {Image} cloudImg
         * @param {number} containerWidth
         */
        function Cloud(canvas, cloudImg, containerWidth) {
          this.canvas = canvas;
          this.canvasCtx = this.canvas.getContext("2d");
          this.image = cloudImg;
          this.containerWidth = containerWidth;
          this.xPos = containerWidth;
          this.yPos = 0;
          this.remove = false;
          this.cloudGap = getRandomNum(Cloud.config.MIN_CLOUD_GAP, Cloud.config.MAX_CLOUD_GAP);

          this.init();
        }

        /**
         * Cloud object config.
         * @enum {number}
         */
        Cloud.config = {
          HEIGHT: 14,
          MAX_CLOUD_GAP: 400,
          MAX_SKY_LEVEL: 30,
          MIN_CLOUD_GAP: 100,
          MIN_SKY_LEVEL: 71,
          WIDTH: 46,
        };

        Cloud.prototype = {
          /**
           * Initialise the cloud. Sets the Cloud height.
           */
          init: function () {
            this.yPos = getRandomNum(Cloud.config.MAX_SKY_LEVEL, Cloud.config.MIN_SKY_LEVEL);
            this.draw();
          },

          /**
           * Draw the cloud.
           */
          draw: function () {
            this.canvasCtx.save();
            var sourceWidth = Cloud.config.WIDTH;
            var sourceHeight = Cloud.config.HEIGHT;

            if (IS_HIDPI) {
              sourceWidth = sourceWidth * 2;
              sourceHeight = sourceHeight * 2;
            }

            this.canvasCtx.drawImage(this.image, 0, 0, sourceWidth, sourceHeight, this.xPos, this.yPos, Cloud.config.WIDTH, Cloud.config.HEIGHT);

            this.canvasCtx.restore();
          },

          /**
           * Update the cloud position.
           * @param {number} speed
           */
          update: function (speed) {
            if (!this.remove) {
              this.xPos -= Math.ceil(speed);
              this.draw();

              // Mark as removeable if no longer in the canvas.
              if (!this.isVisible()) {
                this.remove = true;
              }
            }
          },

          /**
           * Check if the cloud is visible on the stage.
           * @return {boolean}
           */
          isVisible: function () {
            return this.xPos + Cloud.config.WIDTH > 0;
          },
        };

        //******************************************************************************

        /**
         * Horizon Line.
         * Consists of two connecting lines. Randomly assigns a flat / bumpy horizon.
         * @param {HTMLCanvasElement} canvas
         * @param {HTMLImage} bgImg Horizon line sprite.
         * @constructor
         */
        function HorizonLine(canvas, bgImg) {
          this.image = bgImg;
          this.canvas = canvas;
          this.canvasCtx = canvas.getContext("2d");
          this.sourceDimensions = {};
          this.dimensions = HorizonLine.dimensions;
          this.sourceXPos = [0, this.dimensions.WIDTH];
          this.xPos = [];
          this.yPos = 0;
          this.bumpThreshold = 0.5;

          this.setSourceDimensions();
          this.draw();
        }

        /**
         * Horizon line dimensions.
         * @enum {number}
         */
        HorizonLine.dimensions = {
          WIDTH: 600,
          HEIGHT: 12,
          YPOS: 127,
        };

        HorizonLine.prototype = {
          /**
           * Set the source dimensions of the horizon line.
           */
          setSourceDimensions: function () {
            for (var dimension in HorizonLine.dimensions) {
              if (IS_HIDPI) {
                if (dimension != "YPOS") {
                  this.sourceDimensions[dimension] = HorizonLine.dimensions[dimension] * 2;
                }
              } else {
                this.sourceDimensions[dimension] = HorizonLine.dimensions[dimension];
              }
              this.dimensions[dimension] = HorizonLine.dimensions[dimension];
            }

            this.xPos = [0, HorizonLine.dimensions.WIDTH];
            this.yPos = HorizonLine.dimensions.YPOS;
          },

          /**
           * Return the crop x position of a type.
           */
          getRandomType: function () {
            return Math.random() > this.bumpThreshold ? this.dimensions.WIDTH : 0;
          },

          /**
           * Draw the horizon line.
           */
          draw: function () {
            this.canvasCtx.drawImage(this.image, this.sourceXPos[0], 0, this.sourceDimensions.WIDTH, this.sourceDimensions.HEIGHT, this.xPos[0], this.yPos, this.dimensions.WIDTH, this.dimensions.HEIGHT);

            this.canvasCtx.drawImage(this.image, this.sourceXPos[1], 0, this.sourceDimensions.WIDTH, this.sourceDimensions.HEIGHT, this.xPos[1], this.yPos, this.dimensions.WIDTH, this.dimensions.HEIGHT);
          },

          /**
           * Update the x position of an indivdual piece of the line.
           * @param {number} pos Line position.
           * @param {number} increment
           */
          updateXPos: function (pos, increment) {
            var line1 = pos;
            var line2 = pos == 0 ? 1 : 0;

            this.xPos[line1] -= increment;
            this.xPos[line2] = this.xPos[line1] + this.dimensions.WIDTH;

            if (this.xPos[line1] <= -this.dimensions.WIDTH) {
              this.xPos[line1] += this.dimensions.WIDTH * 2;
              this.xPos[line2] = this.xPos[line1] - this.dimensions.WIDTH;
              this.sourceXPos[line1] = this.getRandomType();
            }
          },

          /**
           * Update the horizon line.
           * @param {number} deltaTime
           * @param {number} speed
           */
          update: function (deltaTime, speed) {
            var increment = Math.floor(speed * (FPS / 1000) * deltaTime);

            if (this.xPos[0] <= 0) {
              this.updateXPos(0, increment);
            } else {
              this.updateXPos(1, increment);
            }
            this.draw();
          },

          /**
           * Reset horizon to the starting position.
           */
          reset: function () {
            this.xPos[0] = 0;
            this.xPos[1] = HorizonLine.dimensions.WIDTH;
          },
        };

        //******************************************************************************

        /**
         * Horizon background class.
         * @param {HTMLCanvasElement} canvas
         * @param {Array<HTMLImageElement>} images
         * @param {object} dimensions Canvas dimensions.
         * @param {number} gapCoefficient
         * @constructor
         */
        function Horizon(canvas, images, dimensions, gapCoefficient) {
          this.canvas = canvas;
          this.canvasCtx = this.canvas.getContext("2d");
          this.config = Horizon.config;
          this.dimensions = dimensions;
          this.gapCoefficient = gapCoefficient;
          this.obstacles = [];
          this.horizonOffsets = [0, 0];
          this.cloudFrequency = this.config.CLOUD_FREQUENCY;

          // Cloud
          this.clouds = [];
          this.cloudImg = images.CLOUD;
          this.cloudSpeed = this.config.BG_CLOUD_SPEED;

          // Horizon
          this.horizonImg = images.HORIZON;
          this.horizonLine = null;

          // Obstacles
          this.obstacleImgs = {
            CACTUS_SMALL: images.CACTUS_SMALL,
            CACTUS_LARGE: images.CACTUS_LARGE,
          };

          this.init();
        }

        /**
         * Horizon config.
         * @enum {number}
         */
        Horizon.config = {
          BG_CLOUD_SPEED: 0.2,
          BUMPY_THRESHOLD: 0.3,
          CLOUD_FREQUENCY: 0.5,
          HORIZON_HEIGHT: 16,
          MAX_CLOUDS: 6,
        };

        Horizon.prototype = {
          /**
           * Initialise the horizon. Just add the line and a cloud. No obstacles.
           */
          init: function () {
            this.addCloud();
            this.horizonLine = new HorizonLine(this.canvas, this.horizonImg);
          },

          /**
           * @param {number} deltaTime
           * @param {number} currentSpeed
           * @param {boolean} updateObstacles Used as an override to prevent
           *     the obstacles from being updated / added. This happens in the
           *     ease in section.
           */
          update: function (deltaTime, currentSpeed, updateObstacles) {
            this.runningTime += deltaTime;
            this.horizonLine.update(deltaTime, currentSpeed);
            this.updateClouds(deltaTime, currentSpeed);

            if (updateObstacles) {
              this.updateObstacles(deltaTime, currentSpeed);
            }
          },

          /**
           * Update the cloud positions.
           * @param {number} deltaTime
           * @param {number} currentSpeed
           */
          updateClouds: function (deltaTime, speed) {
            var cloudSpeed = (this.cloudSpeed / 1000) * deltaTime * speed;
            var numClouds = this.clouds.length;

            if (numClouds) {
              for (var i = numClouds - 1; i >= 0; i--) {
                this.clouds[i].update(cloudSpeed);
              }

              var lastCloud = this.clouds[numClouds - 1];

              // Check for adding a new cloud.
              if (numClouds < this.config.MAX_CLOUDS && this.dimensions.WIDTH - lastCloud.xPos > lastCloud.cloudGap && this.cloudFrequency > Math.random()) {
                this.addCloud();
              }

              // Remove expired clouds.
              this.clouds = this.clouds.filter(function (obj) {
                return !obj.remove;
              });
            }
          },

          /**
           * Update the obstacle positions.
           * @param {number} deltaTime
           * @param {number} currentSpeed
           */
          updateObstacles: function (deltaTime, currentSpeed) {
            // Obstacles, move to Horizon layer.
            var updatedObstacles = this.obstacles.slice(0);

            for (var i = 0; i < this.obstacles.length; i++) {
              var obstacle = this.obstacles[i];
              obstacle.update(deltaTime, currentSpeed);

              // Clean up existing obstacles.
              if (obstacle.remove) {
                updatedObstacles.shift();
              }
            }
            this.obstacles = updatedObstacles;

            if (this.obstacles.length > 0) {
              var lastObstacle = this.obstacles[this.obstacles.length - 1];

              if (lastObstacle && !lastObstacle.followingObstacleCreated && lastObstacle.isVisible() && lastObstacle.xPos + lastObstacle.width + lastObstacle.gap < this.dimensions.WIDTH) {
                this.addNewObstacle(currentSpeed);
                lastObstacle.followingObstacleCreated = true;
              }
            } else {
              // Create new obstacles.
              this.addNewObstacle(currentSpeed);
            }
          },

          /**
           * Add a new obstacle.
           * @param {number} currentSpeed
           */
          addNewObstacle: function (currentSpeed) {
            var obstacleTypeIndex = getRandomNum(0, Obstacle.types.length - 1);
            var obstacleType = Obstacle.types[obstacleTypeIndex];
            var obstacleImg = this.obstacleImgs[obstacleType.type];

            this.obstacles.push(new Obstacle(this.canvasCtx, obstacleType, obstacleImg, this.dimensions, this.gapCoefficient, currentSpeed));
          },

          /**
           * Reset the horizon layer.
           * Remove existing obstacles and reposition the horizon line.
           */
          reset: function () {
            this.obstacles = [];
            this.horizonLine.reset();
          },

          /**
           * Update the canvas width and scaling.
           * @param {number} width Canvas width.
           * @param {number} height Canvas height.
           */
          resize: function (width, height) {
            this.canvas.width = width;
            this.canvas.height = height;
          },

          /**
           * Add a new cloud to the horizon.
           */
          addCloud: function () {
            this.clouds.push(new Cloud(this.canvas, this.cloudImg, this.dimensions.WIDTH));
          },
        };
      })();
    </script>
  </head>
  <body id="t" class="offline" style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif; font-size: 75%;">
    <div id="main-frame-error" class="interstitial-wrapper">
      <div id="main-content">
        <img class="icon icon-offline" jseval="updateIconClass(this.classList, iconClass)" style="visibility: hidden;" />
        <div id="main-content" style="font-size: 15px;">
          <h1 style="color: rgb(32, 33, 36); font-weight: 500;">No internet</h1>
          <div style="color: rgb(95, 99, 104);">
            <p style="margin-bottom: 0;">
              Try:
            </p>
            <ul style="margin-top: 0;">
              <li>Checking the network cables, modem, and router</li>
              <li>Reconnecting to Wi-Fi</li>
            </ul>
            <p style="font-size: 12px;" jscontent="errorCode"></p>
           </div>
          </div>
        </div>
      </div>
      <div class="runner-container" style="width: 600px; height: 150px;"><canvas class="runner-canvas" width="1200" height="300" style="width: 600px; height: 150px;"></canvas></div>
    </div>
    <div id="sub-frame-error">
      <!-- Show details when hovering over the icon, in case the details are
         hidden because they're too large. -->
      <img class="icon icon-offline" jseval="updateIconClass(this.classList, iconClass)" jsvalues=".title:errorDetails" title="There is no Internet connection." />
      <div id="sub-frame-error-details" jsvalues=".innerHTML:errorDetails">There is no Internet connection.</div>
    </div>

    <div id="offline-resources">
      <div id="offline-resources-1x">
        <img
          id="1x-obstacle-large"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJYAAAAyCAMAAACJUtIoAAAACVBMVEX////39/dTU1OabbyfAAAAAXRSTlMAQObYZgAAAXhJREFUeF7t2NGqAjEMANGM///RlwvaYQndULuFPJgHUYaEI6IPhgNAOA8HZ+3U6384F5y1U6YzAZTWG+dZamnFEstBFtCKJZSHWMADLJ18z+JqpQeLdKoDC8siC5iFCQs4znIxB5B1t6F3lQWkL4N0JsF+u6GXJdbI+FKW+yWr3lhgCZ2VSag3Nlk/FnRkIRbasLCO0oulikMsvmGpeiGLZ1jOMgtIP5bODivYYUXEIVbwFCt4khVssRgsgidZwQaLd2A8m7MYLGTl4KeQQs2y4kMAMGGlmQViDIb5O6xZnnLD485dIBzqDSE1yyFdL4Iqu4XJqUUWl/NVAFSZq1P6a5aqbAUM2epQbBioWflUBABiUyhYyZoCBev8XyMAObDNOhOAfiyxmHU0YNlldGAphGjFCjA3YkUn1o/1Y3EkZFZ5isCC6NUgwDBn1RuXH96doNfAhDXfsIyJ2AnolcCVhay0kcYbW0HvCO8OwIcJ3GzkORpkFuUP/1Ec8FW1qJkAAAAASUVORK5CYII="
        />
        <img
          id="1x-obstacle-small"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGYAAAAjCAMAAABRlI+PAAAADFBMVEX////////39/dTU1PhglcSAAAAAXRSTlMAQObYZgAAAPNJREFUeF7tlkEKwzAMBLXr//+5iQhU7gRRQkyhZI+DhwH74jhmO+oIJBVwURljuAXagG5QqkSgBLqg3JnxJ1Cb8SmQ3o6gpO85owGlOB4m2BNKJ11BSd01owGlOHkcIAuHkz6UNpPKgozPM54dADHjJuNhZiJxdQCQgZJeBczgCAAy3yhPJvcnmdC9mZwBIsQMFV5AkzHBNknFgcKM+oyDIFcfCAoy03m+jSMIcmoVZkKqSjr1fghyahRmoKRUHYLiSI1SMlCq5CDgX6BXmKkfn+oQ0KEyyrzoy8GbXJ9xrM/YjhUZgl9nnsyTCe9rgSRdV15CwRcIEu8GGQAAAABJRU5ErkJggg=="
        />
        <img
          id="1x-cloud"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAC4AAAAOCAQAAAD6HOaKAAAAU0lEQVR4XrWSsQkAQAgD3X9El/ELixQpJHCfdApnUCtXz7o49cgagaGPaq4rIwAP9s/C7R7UX3inJ0BDb6qWDC7ScOR/QWjRlFizuPwLtTLj+qkH6DjD2wLtikUAAAAASUVORK5CYII="
        />
        <img
          id="1x-text"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAL8AAAAYAQMAAACRPb4TAAAABlBMVEX///9TU1NYzE1OAAAAAXRSTlMAQObYZgAAAPBJREFUeF6lzzFqwzAUx+F/0eBN7wIBXcGjQk3V2/QAHZohEAfv7nU6lUKGbD7DAxe62Soe6lAjtRLGiQOGQh8aHnyCHw+ZSD4dmUPntqpaO0yzIzo5Y46d86a5hAeSemV0IspaNzo9Q11gkz6ZCqvuGkQ/fJnWZt60/Rzs8IHWplt1Bcmb9Hmj+TmfNbqCDqV/CbCfwaMgUSb6F4p9dQmZak9Doo6Wd0qu3TL8YxRDAczwDIgeUoIcqF8GDdzm+GYwACnjiwuP3/8ONY/g8wj0GgLybsy+T43QB8gug+ZgPMGNjY0NVITzHbgHudBYgh9W5adHzknZVQAAAABJRU5ErkJggg=="
        />
        <img
          id="1x-horizon"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABLAAAAAMAgMAAAAPCKxBAAAABlBMVEX///9TU1NYzE1OAAAAAXRSTlMAQObYZgAAALJJREFUeF7t1EEKAyEMhtEvMNm7sPfJEVyY+1+ltLgYAsrQCtWhbxEhQvgxIJtSZypxa/WGshgzKdbq/UihMFMlt3o/CspEYoihIMaAb6mCvM6C+BTAeyo+wN4yykV/6pVfkdLpVyI1hh7GJ6QunUoLEQlQglNP2nkQkeF8+ei9cLxMue1qxVRfk1Ej0s6AEGWfVOk0QUtnK5Xo0Lac6wpdtnQqB6VxomPaz+dgF1PaqqmeWJlz1jYUaSIAAAAASUVORK5CYII="
        />
        <img
          id="1x-trex"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAQgAAAAvAgMAAABiRrxWAAAADFBMVEX///9TU1P39/f///+TS9URAAAAAXRSTlMAQObYZgAAAPpJREFUeF7d0jFKRkEMhdGLMM307itNLALyVmHvJuzTDMjdn72E95PGFEZSmeoU4YMMgxhskvQec8YSVFX1NhGcS5ywtbmC8khcZeKq+ZWJ4F8Sr2+ZCErjkJFEfcjAc/6/BMlfcz6xHdhRthYzIZhIHMcTVY1scUUiAphK8CMSPUbieTBhvD9Lj0vyV4wklEGzHpciKGOJoBp7XDcFs4kWxxM7Ey3iZ8JbzASAvMS7XLOJHTTvEkEZSeQl7DMuwVyCasqK5+XzQRYLUJlMbPXjFcn3m8eKBSjWZMJwvGIOvViAzCbUj1VEDoqFOEQGE3SyInJQLOQMJL4B7enP1UbLXJQAAAAASUVORK5CYII="
        />
        <img
          id="1x-restart"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACQAAAAgCAQAAADQmBIFAAAAZklEQVR4Xu3WMQoAIAxDUe/Y+58jYwV1CwQJWQT5o/DAoaWjV2i/LRym/A5FjEsR41LPQchByEHwIVAEC4gZpghmSDP8egXpr/hQZaAKQFQe+pBOQAblDC336qrlPpSg0MEjInbWTLFFmwc8TpTAAAAAAElFTkSuQmCC"
        />
      </div>
      <div id="offline-resources-2x">
        <img
          id="2x-obstacle-large"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAASwAAABkBAMAAADOLxDzAAAACVBMVEX///9TU1P39/ea77PDAAAAAXRSTlMAQObYZgAAAa9JREFUeF7t1lFqhEAQBuG+wl6h7n/IEEgKlma2R8Vk1O4HWSh++Xzb8AKA8E4IXrlYnsXr+zgh1OdifZbBdFIApdWiWShtVhmQ+jAWMLFollCOsTzgxiyd7GcR01/YLOZf1SwsN2EBozBgAU9l4TAHkDWzCNjKApZlybO4z+GtFwu9bGKZl2TJSyxDxaoX8yyha7LGZRDqxR+ymtUsaNaWhTM+s5rl05tjNUsVz2Kxi6XqhSy4NcvbzgLSnzzvjqzgCCsiHsXSdZwVPIAVHGIhi+ABrOAAi5+Avy7HQhaycpAVpDDBsuKDAOBCrHzjQHgYhl9YsHxf+vRrsQxjVVAsDNMsF6uydBUhq+wWBq/ayCKWZekqA6DKPPEq/ZMsYllWdgGDoMdaLAzMsFwszgoAi1pDxUrWFKhZLlZnpXIkAORAs7YEoFmzQSxmt2NWs+xOP7GapRCiZjUrwFyymhX/xmpWs5rVrGZxQphmsT6LAAsvdgcBhmmWi9VZvN7+x+4K2WtgwBosFmZZvIh9IXsl8M5C1mCxLsvTfizoxfDTAfgdAIPFlVhxRqgHlrVZX9y44aEEvVqmAAAAAElFTkSuQmCC"
        />
        <img
          id="2x-obstacle-small"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMwAAABGBAMAAAByJ2Z/AAAADFBMVEX///9TU1P39/f///+TS9URAAAAAXRSTlMAQObYZgAAARZJREFUeF7t2NEJwzAQg2GtcCtoBe2/W6k5aK8qLgR6ToL9KPzzgR+NPCRRjg2ScjiQ9DKMCE4HRYQOJB2MJyXyQWPQgeSCDD8HnYHh10F6NbJk9KyMwpJ+hkEfnoSyGX1NUmAOqVjSz4zrNgwhm9FbMmEyuS7DpQw/Gf5kOGEYXMgwWBobnGHQmZKsYuyKDcZk8gdmM5uJMzKbgS7I5KENgJzxxN95PUMfAKi8gCXO6BQM4cM4ysEZwplyfxFDErAhmWniDKT3pJEpD2RDMpPEGUt6mOIQ1XFGmiXOZNLIgKUpgzH4lTgDtDIgmY0NznhSnWhk/v2ZkuONGOI2DEn0MNf7ttvMZjazmc2AJDkdJOlQ0sk8AC45t4r28J0GAAAAAElFTkSuQmCC"
        />
        <img
          id="2x-cloud"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAFwAAAAcAgMAAACR2TCnAAAABlBMVEUAAADa2to4qB92AAAAAXRSTlMAQObYZgAAAFFJREFUeF6VzTEKAFEIxNA03m+a3P8q2wqi/E35BIdeGXq3q5hnrwBs7mC5vIZzu/nnqI319vRtqHB731blwSHjx+22+Rdn94rzQq0ugKPVlz5onyJcGdu0NgAAAABJRU5ErkJggg=="
        />
        <img
          id="2x-text"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAX4AAAAwAQMAAAAsMYMXAAAABlBMVEX///9TU1NYzE1OAAAAAXRSTlMAQObYZgAAAPxJREFUeF7tk0FqBCEQRf/gwt14BK+RlV4p2Te0OUFfSZiLmFvUQvzpQgYbOqtA7FnkLz7FhydUlQUr8Ck2w3prjsXuVqMYFrEPVpw0AXgLWJO4bPTxhAiXqtzVbPbpEkCc5nG3GByLAKbwBQDbsBYJQGXTKYthJS8FogD6JOrOL/iiVvYqIN7hE3W/CC51oOjirwNsH+GDBcGwxIYFeh6p38ME4Ff6l6GoN63rTWtqovLMh7B7ngD0I/Fb1nQTxaDq/PBnMgEYFUC+BuDkPLsjwG2E1U0Bju1+nHt47hsqNkwA/KecJjiA8S97suYJgOEAfrwHvGM06eTvgW+oln6hOpuT1AAAAABJRU5ErkJggg=="
        />
        <img
          id="2x-horizon"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAACWAAAAAYAQMAAABEalRSAAAABlBMVEX///9TU1NYzE1OAAAAAXRSTlMAQObYZgAAAOtJREFUeF7tljEKwzAMRb/J0CWgI/QKOYAh1+pUcjQfpUfw2MFEHVyDQSQmQUNM9AYNcobnh4egU+YVqhAvZSpgsfolPnSv5d0nz3vHslgUdK81RLzyvHcsi+WBNxQh4Ln8pw4Wi7skAg9mXgHMrEACXJnbHIllsbqGAtwXhnYswzFzwPWxWEPc2CexoobkHM4ZpD6s2loWiyIEEwCChIomMiMEHqgP573C9eHkc5VLWh3XsljnGVoLWVl+31bp38piTVVuihtPOAm9kcRLbrFjEvqwamtZLK5eI8sSan9rXEK0LcNFrY5oWawf59S7YSRD7eMAAAAASUVORK5CYII="
        />
        <img
          id="2x-trex"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAhAAAABeAgMAAAAPo8UvAAAADFBMVEX///9TU1P39/f///+TS9URAAAAAXRSTlMAQObYZgAAASdJREFUeF7t1qFOBEEQRdEyGP7vGQy/hsHc/0MPSe8ylU2vKEIqqQnviRZXdI7pyUQuONda901FGAG6j8aa+6mDEUboHP01sk5EHHWEjt/UY0dk/U+Ir/cdkXUEovV1GFF/HQMR/mLWEUYYYQRrf65XRhgB2595Y80lYRjCCG7AV/IZ0FdDabgDhiKMgE+tAX01ES+ajDBCADpHZw0tRdaZCCNEGhCdNSSlQTEVYUROQGeNxxoxH2EErXU+wohdQXONqyBorDsixiB2Be01JiOM2BXQX1MRUxFGpAL6aypiMsIIJCFBtSK98fFYKd6wFDEbYUQgEYh6hTSkonbDDTAdYQTrKNd9QPWGUFwAYYRYR7U+XemGfB0ajTACWEe1Pl3thtxMhBHfOCEbEnR2KZcAAAAASUVORK5CYII="
        />
        <img
          id="2x-restart"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABAAgMAAADE0Nm5AAAACVBMVEX////39/dTU1OabbyfAAAAAXRSTlMAQObYZgAAAGNJREFUeF7d1CEOwDAMQ9GS3q/ExPcz8Sm3gYBWVRo0afvwSQl0ax1To22JntKWupfGjriSXiLViCXCmXBHCykJTxaYEeIQGcVrHYklcoX8YYpSUggzcpBTiv5JtQWorUltmS6s4ZKtz2GgjAAAAABJRU5ErkJggg=="
        />
      </div>
      <template id="audio-resources">
        <audio
          id="offline-sound-press"
          src="data:audio/mpeg;base64,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"
        ></audio>
        <audio
          id="offline-sound-hit"
          src="data:audio/mpeg;base64,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"
        ></audio>
        <audio
          id="offline-sound-reached"
          src="data:audio/mpeg;base64,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"
        ></audio>
      </template>
    </div>

    <script>
      // Copyright (c) 2012 The Chromium Authors. All rights reserved.
      // Use of this source code is governed by a BSD-style license that can be
      // found in the LICENSE file.

      /**
       * @fileoverview This file defines a singleton which provides access to all data
       * that is available as soon as the page's resources are loaded (before DOM
       * content has finished loading). This data includes both localized strings and
       * any data that is important to have ready from a very early stage (e.g. things
       * that must be displayed right away).
       */

      var loadTimeData;

      // Expose this type globally as a temporary work around until
      // https://github.com/google/closure-compiler/issues/544 is fixed.
      /** @constructor */
      function LoadTimeData() {}

      (function () {
        "use strict";

        LoadTimeData.prototype = {
          /**
           * Sets the backing object.
           *
           * Note that there is no getter for |data_| to discourage abuse of the form:
           *
           *     var value = loadTimeData.data()['key'];
           *
           * @param {Object} value The de-serialized page data.
           */
          set data(value) {
            expect(!this.data_, "Re-setting data.");
            this.data_ = value;
          },

          /**
           * Returns a JsEvalContext for |data_|.
           * @returns {JsEvalContext}
           */
          createJsEvalContext: function () {
            return new JsEvalContext(this.data_);
          },

          /**
           * @param {string} id An ID of a value that might exist.
           * @return {boolean} True if |id| is a key in the dictionary.
           */
          valueExists: function (id) {
            return id in this.data_;
          },

          /**
           * Fetches a value, expecting that it exists.
           * @param {string} id The key that identifies the desired value.
           * @return {*} The corresponding value.
           */
          getValue: function (id) {
            expect(this.data_, "No data. Did you remember to include strings.js?");
            var value = this.data_[id];
            expect(typeof value != "undefined", "Could not find value for " + id);
            return value;
          },

          /**
           * As above, but also makes sure that the value is a string.
           * @param {string} id The key that identifies the desired string.
           * @return {string} The corresponding string value.
           */
          getString: function (id) {
            var value = this.getValue(id);
            expectIsType(id, value, "string");
            return /** @type {string} */ (value);
          },

          /**
           * Returns a formatted localized string where $1 to $9 are replaced by the
           * second to the tenth argument.
           * @param {string} id The ID of the string we want.
           * @param {...string} var_args The extra values to include in the formatted
           *     output.
           * @return {string} The formatted string.
           */
          getStringF: function (id, var_args) {
            var value = this.getString(id);
            if (!value) return "";

            var varArgs = arguments;
            return value.replace(/\$[$1-9]/g, function (m) {
              return m == "$$" ? "$" : varArgs[m[1]];
            });
          },

          /**
           * As above, but also makes sure that the value is a boolean.
           * @param {string} id The key that identifies the desired boolean.
           * @return {boolean} The corresponding boolean value.
           */
          getBoolean: function (id) {
            var value = this.getValue(id);
            expectIsType(id, value, "boolean");
            return /** @type {boolean} */ (value);
          },

          /**
           * As above, but also makes sure that the value is an integer.
           * @param {string} id The key that identifies the desired number.
           * @return {number} The corresponding number value.
           */
          getInteger: function (id) {
            var value = this.getValue(id);
            expectIsType(id, value, "number");
            expect(value == Math.floor(value), "Number isn't integer: " + value);
            return /** @type {number} */ (value);
          },

          /**
           * Override values in loadTimeData with the values found in |replacements|.
           * @param {Object} replacements The dictionary object of keys to replace.
           */
          overrideValues: function (replacements) {
            expect(typeof replacements == "object", "Replacements must be a dictionary object.");
            for (var key in replacements) {
              this.data_[key] = replacements[key];
            }
          },
        };

        /**
         * Checks condition, displays error message if expectation fails.
         * @param {*} condition The condition to check for truthiness.
         * @param {string} message The message to display if the check fails.
         */
        function expect(condition, message) {
          if (!condition) {
            console.error("Unexpected condition on " + document.location.href + ": " + message);
          }
        }

        /**
         * Checks that the given value has the given type.
         * @param {string} id The id of the value (only used for error message).
         * @param {*} value The value to check the type on.
         * @param {string} type The type we expect |value| to be.
         */
        function expectIsType(id, value, type) {
          expect(typeof value == type, "[" + value + "] (" + id + ") is not a " + type);
        }

        expect(!loadTimeData, "should only include this file once");
        loadTimeData = new LoadTimeData();
      })();
    </script>
    <script>
      loadTimeData.data = {
        details: "Details",
        errorCode: "ERR_INTERNET_DISCONNECTED",
        errorDetails: "The Internet connection has been lost.",
        fontfamily: "'Helvetica Neue', 'Lucida Grande', sans-serif",
        fontsize: "75%",
        heading: "Unable to connect to the Internet",
        hideDetails: "Hide details",
        iconClass: "icon-offline",
        language: "en",
        primaryParagraph: "Google Chrome can’t display the webpage because your computer isn’t connected to the Internet.",
        suggestions: [],
        summary: {
          failedUrl: "https://www.facebook.com/",
          hostName: "www.facebook.com",
          msg:
            "You can try to diagnose the problem by taking the following steps:\n          \u003Cbr />\n          Go to\n          \u003Cstrong>\n          Applications > System Preferences > Network > Assist me\n          \u003C/strong>\n          to test your connection.",
          productName: "Google Chrome",
        },
        textdirection: "ltr",
        title: "https://www.facebook.com/ is not available",
      };
    </script>
    <script>
      // Copyright (c) 2012 The Chromium Authors. All rights reserved.
      // Use of this source code is governed by a BSD-style license that can be
      // found in the LICENSE file.

      // Copyright (c) 2012 The Chromium Authors. All rights reserved.
      // Use of this source code is governed by a BSD-style license that can be
      // found in the LICENSE file.

      /**
       * @fileoverview This is a simple template engine inspired by JsTemplates
       * optimized for i18n.
       *
       * It currently supports three handlers:
       *
       *   * i18n-content which sets the textContent of the element.
       *
       *     <span i18n-content="myContent"></span>
       *
       *   * i18n-options which generates <option> elements for a <select>.
       *
       *     <select i18n-options="myOptionList"></select>
       *
       *   * i18n-values is a list of attribute-value or property-value pairs.
       *     Properties are prefixed with a '.' and can contain nested properties.
       *
       *     <span i18n-values="title:myTitle;.style.fontSize:fontSize"></span>
       *
       * This file is a copy of i18n_template.js, with minor tweaks to support using
       * load_time_data.js. It should replace i18n_template.js eventually.
       */

      var i18nTemplate = (function () {
        /**
         * This provides the handlers for the templating engine. The key is used as
         * the attribute name and the value is the function that gets called for every
         * single node that has this attribute.
         * @type {!Object}
         */
        var handlers = {
          /**
           * This handler sets the textContent of the element.
           * @param {HTMLElement} element The node to modify.
           * @param {string} key The name of the value in the dictionary.
           * @param {LoadTimeData} dictionary The dictionary of strings to draw from.
           */
          "i18n-content": function (element, key, dictionary) {
            element.textContent = dictionary.getString(key);
          },

          /**
           * This handler adds options to a <select> element.
           * @param {HTMLElement} select The node to modify.
           * @param {string} key The name of the value in the dictionary. It should
           *     identify an array of values to initialize an <option>. Each value,
           *     if a pair, represents [content, value]. Otherwise, it should be a
           *     content string with no value.
           * @param {LoadTimeData} dictionary The dictionary of strings to draw from.
           */
          "i18n-options": function (select, key, dictionary) {
            var options = dictionary.getValue(key);
            options.forEach(function (optionData) {
              var option = typeof optionData == "string" ? new Option(optionData) : new Option(optionData[1], optionData[0]);
              select.appendChild(option);
            });
          },

          /**
           * This is used to set HTML attributes and DOM properties. The syntax is:
           *   attributename:key;
           *   .domProperty:key;
           *   .nested.dom.property:key
           * @param {HTMLElement} element The node to modify.
           * @param {string} attributeAndKeys The path of the attribute to modify
           *     followed by a colon, and the name of the value in the dictionary.
           *     Multiple attribute/key pairs may be separated by semicolons.
           * @param {LoadTimeData} dictionary The dictionary of strings to draw from.
           */
          "i18n-values": function (element, attributeAndKeys, dictionary) {
            var parts = attributeAndKeys.replace(/\s/g, "").split(/;/);
            parts.forEach(function (part) {
              if (!part) return;

              var attributeAndKeyPair = part.match(/^([^:]+):(.+)$/);
              if (!attributeAndKeyPair) throw new Error("malformed i18n-values: " + attributeAndKeys);

              var propName = attributeAndKeyPair[1];
              var propExpr = attributeAndKeyPair[2];

              var value = dictionary.getValue(propExpr);

              // Allow a property of the form '.foo.bar' to assign a value into
              // element.foo.bar.
              if (propName[0] == ".") {
                var path = propName.slice(1).split(".");
                var targetObject = element;
                while (targetObject && path.length > 1) {
                  targetObject = targetObject[path.shift()];
                }
                if (targetObject) {
                  targetObject[path] = value;
                  // In case we set innerHTML (ignoring others) we need to
                  // recursively check the content.
                  if (path == "innerHTML") process(element, dictionary);
                }
              } else {
                element.setAttribute(propName, /** @type {string} */ (value));
              }
            });
          },
        };

        var attributeNames = Object.keys(handlers);
        var selector = "[" + attributeNames.join("],[") + "]";

        /**
         * Processes a DOM tree with the {@code dictionary} map.
         * @param {HTMLElement} node The root of the DOM tree to process.
         * @param {LoadTimeData} dictionary The dictionary to draw from.
         */
        function process(node, dictionary) {
          var elements = node.querySelectorAll(selector);
          for (var element, i = 0; (element = elements[i]); i++) {
            for (var j = 0; j < attributeNames.length; j++) {
              var name = attributeNames[j];
              var attribute = element.getAttribute(name);
              if (attribute != null) handlers[name](element, attribute, dictionary);
            }
          }
        }

        return {
          process: process,
        };
      })();

      i18nTemplate.process(document, loadTimeData);
    </script>
    <script>
      // Copyright (c) 2012 The Chromium Authors. All rights reserved.
      // Use of this source code is governed by a BSD-style license that can be
      // found in the LICENSE file.

      // This file serves as a proxy to bring the included js file from /third_party
      // into its correct location under the resources directory tree, whence it is
      // delivered via a chrome://resources URL.  See ../webui_resources.grd.
      (function () {
        var i = null;
        function k() {
          return Function.prototype.call.apply(Array.prototype.slice, arguments);
        }
        function l(a, b) {
          var c = k(arguments, 2);
          return function () {
            return b.apply(a, c);
          };
        }
        function m(a, b) {
          var c = new n(b);
          for (c.f = [a]; c.f.length; ) {
            var e = c,
              d = c.f.shift();
            e.g(d);
            for (d = d.firstChild; d; d = d.nextSibling) d.nodeType == 1 && e.f.push(d);
          }
        }
        function n(a) {
          this.g = a;
        }
        function o(a) {
          a.style.display = "";
        }
        function p(a) {
          a.style.display = "none";
        }
        var q = ":",
          r = /\s*;\s*/;
        function s() {
          this.i.apply(this, arguments);
        }
        s.prototype.i = function (a, b) {
          if (!this.a) this.a = {};
          if (b) {
            var c = this.a,
              e = b.a,
              d;
            for (d in e) c[d] = e[d];
          } else for (c in ((d = this.a), (e = t), e)) d[c] = e[c];
          this.a.$this = a;
          this.a.$context = this;
          this.d = typeof a != "undefined" && a != i ? a : "";
          if (!b) this.a.$top = this.d;
        };
        var t = { $default: i },
          u = [];
        function v(a) {
          for (var b in a.a) delete a.a[b];
          a.d = i;
          u.push(a);
        }
        function w(a, b, c) {
          try {
            return b.call(c, a.a, a.d);
          } catch (e) {
            return t.$default;
          }
        }
        function x(a, b, c, e) {
          if (u.length > 0) {
            var d = u.pop();
            s.call(d, b, a);
            a = d;
          } else a = new s(b, a);
          a.a.$index = c;
          a.a.$count = e;
          return a;
        }
        var y = "a_",
          z = "b_",
          A = "with (a_) with (b_) return ",
          D = {};
        function E(a) {
          if (!D[a])
            try {
              D[a] = new Function(y, z, A + a);
            } catch (b) {}
          return D[a];
        }
        function F(a) {
          for (var b = [], a = a.split(r), c = 0, e = a.length; c < e; ++c) {
            var d = a[c].indexOf(q);
            if (!(d < 0)) {
              var f;
              f = a[c].substr(0, d).replace(/^\s+/, "").replace(/\s+$/, "");
              d = E(a[c].substr(d + 1));
              b.push(f, d);
            }
          }
          return b;
        }
        var G = "jsinstance",
          H = "jsts",
          I = "*",
          J = "div",
          K = "id";
        function L() {}
        var M = 0,
          N = { 0: {} },
          P = {},
          Q = {},
          R = [];
        function S(a) {
          a.__jstcache ||
            m(a, function (a) {
              T(a);
            });
        }
        var U = [
          ["jsselect", E],
          ["jsdisplay", E],
          ["jsvalues", F],
          ["jsvars", F],
          [
            "jseval",
            function (a) {
              for (var b = [], a = a.split(r), c = 0, e = a.length; c < e; ++c)
                if (a[c]) {
                  var d = E(a[c]);
                  b.push(d);
                }
              return b;
            },
          ],
          [
            "transclude",
            function (a) {
              return a;
            },
          ],
          ["jscontent", E],
          ["jsskip", E],
        ];
        function T(a) {
          if (a.__jstcache) return a.__jstcache;
          var b = a.getAttribute("jstcache");
          if (b != i) return (a.__jstcache = N[b]);
          for (var b = (R.length = 0), c = U.length; b < c; ++b) {
            var e = U[b][0],
              d = a.getAttribute(e);
            Q[e] = d;
            d != i && R.push(e + "=" + d);
          }
          if (R.length == 0) return a.setAttribute("jstcache", "0"), (a.__jstcache = N[0]);
          var f = R.join("&");
          if ((b = P[f])) return a.setAttribute("jstcache", b), (a.__jstcache = N[b]);
          for (var h = {}, b = 0, c = U.length; b < c; ++b) {
            var d = U[b],
              e = d[0],
              g = d[1],
              d = Q[e];
            d != i && (h[e] = g(d));
          }
          b = "" + ++M;
          a.setAttribute("jstcache", b);
          N[b] = h;
          P[f] = b;
          return (a.__jstcache = h);
        }
        function V(a, b) {
          a.h.push(b);
          a.k.push(0);
        }
        function W(a) {
          return a.c.length ? a.c.pop() : [];
        }
        L.prototype.e = function (a, b) {
          var c = X(b),
            e = c.transclude;
          if (e) (c = Y(e)) ? (b.parentNode.replaceChild(c, b), (e = W(this)), e.push(this.e, a, c), V(this, e)) : b.parentNode.removeChild(b);
          else if ((c = c.jsselect)) {
            var c = w(a, c, b),
              d = b.getAttribute(G),
              f = !1;
            d && (d.charAt(0) == I ? ((d = parseInt(d.substr(1), 10)), (f = !0)) : (d = parseInt(d, 10)));
            var h = c != i && typeof c == "object" && typeof c.length == "number",
              e = h ? c.length : 1,
              g = h && e == 0;
            if (h)
              if (g) d ? b.parentNode.removeChild(b) : (b.setAttribute(G, "*0"), p(b));
              else if ((o(b), d === i || d === "" || (f && d < e - 1))) {
                f = W(this);
                d = d || 0;
                for (h = e - 1; d < h; ++d) {
                  var j = b.cloneNode(!0);
                  b.parentNode.insertBefore(j, b);
                  Z(j, c, d);
                  g = x(a, c[d], d, e);
                  f.push(this.b, g, j, v, g, i);
                }
                Z(b, c, d);
                g = x(a, c[d], d, e);
                f.push(this.b, g, b, v, g, i);
                V(this, f);
              } else d < e ? ((f = c[d]), Z(b, c, d), (g = x(a, f, d, e)), (f = W(this)), f.push(this.b, g, b, v, g, i), V(this, f)) : b.parentNode.removeChild(b);
            else c == i ? p(b) : (o(b), (g = x(a, c, 0, 1)), (f = W(this)), f.push(this.b, g, b, v, g, i), V(this, f));
          } else this.b(a, b);
        };
        L.prototype.b = function (a, b) {
          var c = X(b),
            e = c.jsdisplay;
          if (e) {
            if (!w(a, e, b)) {
              p(b);
              return;
            }
            o(b);
          }
          if ((e = c.jsvars))
            for (var d = 0, f = e.length; d < f; d += 2) {
              var h = e[d],
                g = w(a, e[d + 1], b);
              a.a[h] = g;
            }
          if ((e = c.jsvalues)) {
            d = 0;
            for (f = e.length; d < f; d += 2)
              if (((g = e[d]), (h = w(a, e[d + 1], b)), g.charAt(0) == "$")) a.a[g] = h;
              else if (g.charAt(0) == ".") {
                for (var g = g.substr(1).split("."), j = b, O = g.length, B = 0, $ = O - 1; B < $; ++B) {
                  var C = g[B];
                  j[C] || (j[C] = {});
                  j = j[C];
                }
                j[g[O - 1]] = h;
              } else g && (typeof h == "boolean" ? (h ? b.setAttribute(g, g) : b.removeAttribute(g)) : b.setAttribute(g, "" + h));
          }
          if ((e = c.jseval)) {
            d = 0;
            for (f = e.length; d < f; ++d) w(a, e[d], b);
          }
          e = c.jsskip;
          if (!e || !w(a, e, b))
            if ((c = c.jscontent)) {
              if (((c = "" + w(a, c, b)), b.innerHTML != c)) {
                for (; b.firstChild; ) (e = b.firstChild), e.parentNode.removeChild(e);
                b.appendChild(this.j.createTextNode(c));
              }
            } else {
              c = W(this);
              for (e = b.firstChild; e; e = e.nextSibling) e.nodeType == 1 && c.push(this.e, a, e);
              c.length && V(this, c);
            }
        };
        function X(a) {
          if (a.__jstcache) return a.__jstcache;
          var b = a.getAttribute("jstcache");
          if (b) return (a.__jstcache = N[b]);
          return T(a);
        }
        function Y(a, b) {
          var c = document;
          if (b) {
            var e = c.getElementById(a);
            if (!e) {
              var e = b(),
                d = H,
                f = c.getElementById(d);
              if (!f) (f = c.createElement(J)), (f.id = d), p(f), (f.style.position = "absolute"), c.body.appendChild(f);
              d = c.createElement(J);
              f.appendChild(d);
              d.innerHTML = e;
              e = c.getElementById(a);
            }
            c = e;
          } else c = c.getElementById(a);
          return c ? (S(c), (c = c.cloneNode(!0)), c.removeAttribute(K), c) : i;
        }
        function Z(a, b, c) {
          c == b.length - 1 ? a.setAttribute(G, I + c) : a.setAttribute(G, "" + c);
        }
        window.jstGetTemplate = Y;
        window.JsEvalContext = s;
        window.jstProcess = function (a, b) {
          var c = new L();
          S(b);
          c.j = b ? (b.nodeType == 9 ? b : b.ownerDocument || document) : document;
          var e = l(c, c.e, a, b),
            d = (c.h = []),
            f = (c.k = []);
          c.c = [];
          e();
          for (var h, g, j; d.length; )
            (h = d[d.length - 1]), (e = f[f.length - 1]), e >= h.length ? ((e = c), (g = d.pop()), (g.length = 0), e.c.push(g), f.pop()) : ((g = h[e++]), (j = h[e++]), (h = h[e++]), (f[f.length - 1] = e), g.call(c, j, h));
        };
      })();
    </script>
    <script>
      var tp = document.getElementById("t");
      jstProcess(loadTimeData.createJsEvalContext(), tp);
      console.error(`Failed to load resource:
net::ERR_INTERNET_DISCONNECTED`)
    </script>
  </body>
</html>
```
