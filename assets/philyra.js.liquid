/* ---GET LIQUID DATA--- */  
    // product.options to get option names
    // product.options_by_name
    const kwToProduct = {"Power Luxe":"power-luxe","POWERLIFT":"power-lift-face-moisturizer"};
    const productDataStorage = {};
    
    const products = [];

    const philyraISO = document.getElementById('philyra-iso-code').value;
    
    /* --- STATISTICS CODE --- */
    const registerMouseHover = async () => {
      const myshopifyDomain = document.getElementById('philyraPermanentDomain').innerHTML;
        const url = 'https://europe-west1-rheia-96aff.cloudfunctions.net/counterService/hover';
        const reqBody = {myshopifyDomain};
        await fetch(url, {
          method: 'POST',
          body: JSON.stringify(reqBody),
        })
        return;
    }
    
    const registerAddToCart = async () => {
      const myshopifyDomain = document.getElementById('philyraPermanentDomain').innerHTML;
        const url = 'https://europe-west1-rheia-96aff.cloudfunctions.net/counterService/addToCart';
        const reqBody = {myshopifyDomain};
        await fetch(url, {
          method: 'POST',
          body: JSON.stringify(reqBody),
        })
        return;
    }
    
    /* ---CAROUSEL CODE--- */
      // could make this a function that I could call on render and 
      // whenever a pop-up is made active
    
    function configurePopup() {
      const selectedPopup = document.querySelector('.philyra__mouse-hover-popup-container');
      const track = selectedPopup.querySelector('.philyra__carousel__track');
      const slides = Array.from(track.children);
      
      const prevButton = selectedPopup.querySelector('.philyra__carousel__button--left');
      const nextButton = selectedPopup.querySelector('.philyra__carousel__button--right');
      
      const slideSize = slides[0].getBoundingClientRect();
      const slideWidth = slideSize?.width ? slideSize?.width : 0;
      
      // Set first slide as initial selected slide
      slides[0].classList.add('philyra__selected-slide');
      prevButton.classList.add('philyra__is-hidden');
      
      const setSlidePosition = (slide, index) => {
        slide.style.left = slideWidth * index + 'px';
      }
      
      // Arrange slides next to one another
      slides.forEach((slide, index) => {
        setSlidePosition(slide, index);
      });
     
      if(slides?.length === 1){
        prevButton.classList.add('philyra__is-hidden');
        nextButton.classList.add('philyra__is-hidden');
      }
      
      // Handle the moving of slides
      const moveToSlide = (track, currentSlide, targetSlide) => {
        track.style.transform = 'translateX(-' + targetSlide.style.left + ')';
        currentSlide.classList.remove('philyra__selected-slide');
        targetSlide.classList.add('philyra__selected-slide');
        
        const targetIndex = slides.findIndex(slide => (slide === targetSlide));
        if(targetIndex === 0) {
          prevButton.classList.add('philyra__is-hidden');
          nextButton.classList.remove('philyra__is-hidden');
        } else if (targetIndex === slides.length - 1) {
          nextButton.classList.add('philyra__is-hidden');
          prevButton.classList.remove('philyra__is-hidden');
        } else {
          prevButton.classList.remove('philyra__is-hidden');
          nextButton.classList.remove('philyra__is-hidden');
        }
      }
      
      nextButton.addEventListener('click', e => {
        const currentSlide = track.querySelector('.philyra__selected-slide');
        const nextSlide = currentSlide.nextElementSibling;
        moveToSlide(track, currentSlide, nextSlide);
      });
      
      prevButton.addEventListener('click', e => {
        const currentSlide = track.querySelector('.philyra__selected-slide');
        const prevSlide = currentSlide.previousElementSibling;
        moveToSlide(track, currentSlide, prevSlide);
      });
    }
    
      /* ---GENERAL CODE--- */
    function addCloseEventListeners() {
      document.querySelectorAll('.philyra__mouse-hover-close-button').forEach(closeButton => {
          closeButton.addEventListener('click', event => {
            const currentPopup = document.querySelector('.philyra__mouse-hover-popup-container');
            
            // reset popup styles
            currentPopup.style.display = 'none';
            currentPopup.style.opacity = '0';
            const pageBody = document.getElementsByTagName('body')[0];
          pageBody.style.overflow = "auto";
            const prevButton = currentPopup.querySelector('.philyra__carousel__button--left');
          const nextButton = currentPopup.querySelector('.philyra__carousel__button--right');
            prevButton.classList.remove('philyra__is-hidden');
            nextButton.classList.remove('philyra__is-hidden');
            
            // restart slides
            const selectedSlide = document.querySelector('.philyra__selected-slide');
            selectedSlide.classList.remove('philyra__selected-slide');
            const track = currentPopup.querySelector('.philyra__carousel__track');
            track.style.removeProperty('transform');
            
            // make sure pop-up animation triggers again
            const newPopup = currentPopup.cloneNode(true);
        currentPopup.parentNode.replaceChild(newPopup, currentPopup);
            addCloseEventListeners();
           
          });
      });
    }
      
       
    
    /* ---KEYWORD REPLACEMENT CODE--- */

    const addProductToProductsArray = (keyword) => {
      const newProduct = kwToProduct[keyword];
      const productIdx = products.findIndex((p) => {
          return p === newProduct;
      });
   
      if(productIdx < 0) {
         products.push(newProduct);
        console.log(products);
      }
    }

    const replaceKeywords = (keywords) => {
      for(j = 0; j < keywords.length; j++){
          const keyword = keywords[j];
            const returnSpan = () => ("<span class='philyra__blog-keyword'>" + keyword + "</span>");
          const regex = new RegExp("(" + keyword + ")(?!([^<]+)?>)");
        
          const main = [...document.getElementsByTagName('main')];
          let text;
          if(main?.length) {
             text = [...main[0].querySelectorAll('p'), ...main[0].querySelectorAll('span')];
           } else {
             text = [...document.querySelectorAll('p'), ...document.querySelectorAll('span')];
           }
        
          // loop through all texts and replace keywords with philyra mouse hover
          for(let i = 0; i < text.length; i++) {
              const p = text[i];
              if(p.innerHTML.match(regex)){
                addProductToProductsArray(keyword);
              }
              p.innerHTML = p.innerHTML.replace(regex, returnSpan());
          }
        }
    }

    const viewProductTranslations = {
      en: 'View product',
      nl: 'Bekijk product',
      de: 'Produkt anzeigen',
      pl: 'Zobacz produkt',
      fr: 'Voir le produit',
      es: 'Ver el producto',
      it: 'Visualizza prodotto',
      pt: 'Ver produto',
      cz: 'Zobrazit produkt',
      dk: 'Se produkt',
      fi: 'Katso tuote',
      se: 'Visa produkt',
      ru: 'Посмотреть продукт',
      gr: 'Προβολή προϊόντος',
      tr: 'Ürünü görüntüle',
    }
             
    const viewProductTranslationText = viewProductTranslations[philyraISO] ? viewProductTranslations[philyraISO] : 'View product';
    
    const replaceTags = (tags) => {
      for(j = 0; j < tags.length; j++){
          const unformattedTag = tags[j];
            const tagFormatOne = unformattedTag.replace("[","\\\[");
            const tag = tagFormatOne.replace("]", "\\\]");
         
          const tagFormatTwo = unformattedTag.replace("[", "");
          const dictTag = tagFormatTwo.replace("]", "");
         
            const returnEmbed = () => {
            const productHandle = kwToProduct[dictTag]
            const thisProductData = productDataStorage[productHandle];
            const imgUrl = "https://uploads-ssl.webflow.com/6044efa8ff1caf830c302fb3/60e572d6d6c7c118245e2e58_image_large.png";
              return '<div class="philyra__product-embed-wrapper"><img class="philyra__product-embed-image" alt="" src=' + imgUrl + ' /><button class="philyra__product-embed-button btn " value=' + dictTag + ' >' + viewProductTranslationText + '</button></div>'
             };
          const regex = new RegExp("(" + tag + ")(?!([^<]+)?>)");
        
          let text;
          const main = [...document.getElementsByTagName('main')];

          if(main?.length) {
            text = [...main[0].querySelectorAll('p'), ...main[0].querySelectorAll('span'), ...main[0].querySelectorAll('center')];
          } else {
            text = [...document.querySelectorAll('p'), ...document.querySelectorAll('span'), ...document.querySelectorAll('center')];
          }
        
          // loop through all texts and replace keywords with philyra mouse hover
          for(let i = 0; i < text.length; i++) {
              const p = text[i];
              if(p.innerHTML.match(regex)){
                addProductToProductsArray(dictTag);
              }
              p.innerHTML = p.innerHTML.replace(regex, returnEmbed());
          }
        }
    }

    const replaceProductEmbedImages = () => {
      const productEmbeds = document.querySelectorAll('.philyra__product-embed-wrapper');
   
       for(let i = 0; i < productEmbeds.length; i++){
           const productEmbedImage = productEmbeds[i].querySelector('.philyra__product-embed-image');
           const productEmbedButton = productEmbeds[i].querySelector('.philyra__product-embed-button');
           const dictTag = productEmbedButton.value;
           const productHandle = kwToProduct[dictTag]
           const thisProductData = productDataStorage[productHandle];
           productEmbedImage.src = thisProductData?.featured_image ? thisProductData?.featured_image : "https://uploads-ssl.webflow.com/6044efa8ff1caf830c302fb3/60e572d6d6c7c118245e2e58_image_large.png";
      }
    }
    
    const kwEventListener = () => { 
        // make page unscrollable
        const pageBody = document.getElementsByTagName('body')[0];
        pageBody.style.overflow = "hidden";
            
        // make pop-up visible
        const currentPopup = document.querySelector('.philyra__mouse-hover-popup-container');
        currentPopup.style.display = 'flex';
        currentPopup.style.opacity = '1';
        // get pop-up ready
        configurePopup();
    }

    const addToCartTranslations = {
      en: 'Add to cart',
      nl: 'Toevoegen aan winkelwagen',
      de: 'In den Warenkorb legen',
      pl: 'Dodaj do koszyka',
      fr: 'Ajouter au panier',
      es: 'Añadir a la cesta',
      it: 'Aggiungi al carrello',
      pt: 'Adicionar ao Carrinho',
      cz: 'Přidat do košíku',
      dk: 'Tilføj til kurv',
      fi: 'Lisää ostoskoriin',
      se: 'Lägg till i kundvagn',
      ru: 'Добавить в корзину',
      gr: 'Προσθήκη στο καλάθι',
      tr: 'Sepete ekle',
    }
    
    const soldOutTranslations = {
      en: 'Sold out',
      nl: 'Uitverkocht',
      de: 'Ausverkauft',
      pl: 'Wyprzedane',
      fr: 'Épuisé',
      es: 'Vendido',
      it: 'Venduto',
      pt: 'Esgotado',
      cz: 'Vyprodáno',
      dk: 'Udsolgt',
      fi: 'Loppuunmyyty',
      se: 'Utsåld',
      ru: 'Распроданный',
      gr: 'Εξαντλημένα',
      tr: 'Tükendi',
    }
    
    const setButtonToSoldOut = (addToCartBtn) => {
      addToCartBtn.classList.add('philyra__sold-out-button');
        addToCartBtn.disabled = true;
        addToCartBtn.innerHTML = soldOutTranslations[philyraISO] ? soldOutTranslations[philyraISO] : 'Sold out';
    }
    
    const setButtonToAvailable = (addToCartBtn) => {
      addToCartBtn.classList.remove('philyra__sold-out-button');
        addToCartBtn.disabled = false;
        addToCartBtn.innerHTML = addToCartTranslations[philyraISO] ? addToCartTranslations[philyraISO] : 'Add to cart';
    }
    
    const assignValueToCartBtn = (val) => {
      const addToCartBtn = document.querySelector('.philyra__add-to-cart-button');
        addToCartBtn.value = val;
    }
    
    const setPrice = (amountInCents) => {
      const priceTag = document.querySelector('.philyra__product-price');
        const currency = document.getElementById('philyraCurrency').innerHTML;
        let formattedCurrency = currency;
        if(currency === "EUR") {formattedCurrency = "€";}
        if(currency === "USD") {formattedCurrency = "$";}
        const newInnerHtml = formattedCurrency + (amountInCents/100).toString();
        priceTag.innerHTML = newInnerHtml;
    }

    const loadingTranslations = {
      en: 'Loading...',
      nl: 'Laden...',
      de: 'Wird geladen...',
      pl: 'Ładowanie...',
      fr: 'Chargement...',
      es: 'Cargando...',
      it: 'Caricamento in corso...',
      pt: 'Carregando...',
      cz: 'Načítání...',
      dk: 'Indlæser...',
      fi: 'Ladataan...',
      se: 'Läser in...',
      ru: 'Загружается ...',
      gr: 'Φόρτωση...',
      tr: 'Yükleniyor...',
    }
    
    const successTranslations = {
      en: 'Success!',
      nl: 'Klaar!',
      de: 'Erfolg!',
      pl: 'Sukces!',
      fr: 'Succès!',
      es: '¡Éxito!',
      it: 'Successo!',
      pt: 'Sucesso!',
      cz: 'Úspěch!',
      dk: 'Succes!',
      fi: 'Menestys!',
      se: 'Framgång!',
      ru: 'Успех!',
      gr: 'Επιτυχία!',
      tr: 'Başarı!',
    }
    
    const handleSubmit = async (productId) => {
      try {
        const addToCartBtn = document.querySelector('.philyra__add-to-cart-button');
        const formData = {
          items: [{id: productId, quantity: 1}],
        };
        
        // adjust button to notify user
        addToCartBtn.disabled = true;
        addToCartBtn.innerHTML = loadingTranslations[philyraISO] ? loadingTranslations[philyraISO] : 'Loading...';
        
        // make fetch
        await fetch('/cart/add.js', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify(formData),
        });
        
        addToCartBtn.innerHTML = successTranslations[philyraISO] ? successTranslations[philyraISO] : 'Success!';
        registerAddToCart();
        
        // reload page so cart updates
        location.reload();
      return false;
      } catch(err) {
        console.log(err.message);
        alert(err.message);
        setButtonToAvailable(document.querySelector('.philyra__add-to-cart-button'));
      }
    }
    
    const addEventListenerToVariantButtons = () => {
      document.querySelectorAll('.philyra__selector').forEach(selector => {
        selector.addEventListener('click', event => {
          // handle old button
          const oldSelectedButton = document.querySelector('.philyra__popup__variant-selector-selected');
          oldSelectedButton.classList.remove('philyra__popup__variant-selector-selected');
          oldSelectedButton.classList.add('philyra__popup__variant-selector');
          // handle new button
          selector.classList.remove('philyra__popup__variant-selector');
          selector.classList.add('philyra__popup__variant-selector-selected');
          assignValueToCartBtn(selector.value);
          
          // get product handle
          const titleTag = document.querySelector('.philyra__popup-product-title');
          const productHandle = titleTag.value;
          
          // get product data
          const productObj = productDataStorage[productHandle];
          const variants = productObj.variants;
          
          const variantId = selector.value;
          const variantObj = variants.find(v => {
            return v.id.toString() === variantId;
          });
    
          if(!variantObj) return;
          
          setPrice(variantObj.price);
          const addToCartBtn = document.querySelector('.philyra__add-to-cart-button');
          variantObj.available ? setButtonToAvailable(addToCartBtn) : setButtonToSoldOut(addToCartBtn);
        });
      });
    }

    const selectVariantTranslations = {
      en: 'Select variant',
      nl: 'Selecteer variant',
      de: 'Variante auswählen',
      pl: 'Wybierz wariant',
      fr: 'Sélectionnez la variante',
      es: 'Seleccionar variante',
      it: 'Seleziona la variante',
      pt: 'Selecione a variante',
      cz: 'Vyberte variantu',
      dk: 'Vælg variant',
      fi: 'Valitse variantti',
      se: 'Välj variant',
      ru: 'Выбрать вариант',
      gr: 'Επιλέξτε παραλλαγή',
      tr: 'Varyant seçin',
    }
    
    const insertProductData = (keyword) => {
       const product = kwToProduct[keyword];
             
       if(!product) {
             alert('Product data not found!');
             return;
       };
       
       const thisProductData = productDataStorage[product];
       
       // get needed data
       const { title, variants, price, available, description, images, options } = thisProductData;
      
       // set price (we'll handle variants later)
       setPrice(price);
       
       // change add to cart button in case product is not available
       const addToCartBtn = document.querySelector('.philyra__add-to-cart-button');
       
       if(!available) {
          setButtonToSoldOut(addToCartBtn);
       } else {
          setButtonToAvailable(addToCartBtn);
       }
      
       // set value of addToCart button (we'll handle variants later)
       assignValueToCartBtn(variants[0].id);
       
       // load images into pop-up
       const track = document.querySelector('.philyra__carousel__track');
       if(images?.length){
          const imgTags = [];
            images.forEach(imgUrl => {
              imgTags.push('<li class="philyra__carousel__slide"><img class="philyra__carousel__image" draggable="false" src=' + imgUrl + ' /> </li>');
            });
            const newSlides = imgTags.join('');
            track.innerHTML = newSlides;
         } else {
          const imgUrl = "https://uploads-ssl.webflow.com/6044efa8ff1caf830c302fb3/60e572d6d6c7c118245e2e58_image_large.png";
          const tag = '<li class="philyra__carousel__slide"><img class="philyra__carousel__image" draggable="false" src=' + imgUrl + ' /> </li>';
          track.innerHTML = tag;
         }
       
       // load title and description
       const titleTag = document.querySelector('.philyra__popup-product-title');
       titleTag.innerHTML = title;
       titleTag.value = product;
       
       const descriptionTag = document.querySelector('.philyra__product-description');
       descriptionTag.innerHTML = description;
       
       if(description === "" && descriptionTag.innerHTML === ""){
         const descriptionHeader = document.querySelector('#philyra__product-description-header');
         descriptionHeader.style.display = 'none';
       }
       
       // handle the 'go to product' tag
       const goToProductTag = document.querySelector('.philyra__go-to-product');
       if(goToProductTag) {
         const baseUrl = document.getElementById('philyraRootUrl').innerHTML;
         const goToProductUrl = baseUrl + '/products' + '/' + product;
         goToProductTag.href = goToProductUrl;
         goToProductTag.target = '_blank';
       }
       
       // handle variants
       const realVariants = variants?.filter(v => {
          return v.title !== 'Default Title';
        });
       const variantsSection = document.getElementById('philyra__variants-section');
       let variantsSectionHtml = '';
       let variantsSectionArray = [];
       
       if(realVariants?.length){
          const selectVariantTranslationText = selectVariantTranslations[philyraISO] ? selectVariantTranslations[philyraISO] : 'Select variant'; 
          variantsSectionArray.push('<div style="margin-bottom: 20px;"><h4 class="philyra__section-title philyra__adopt-heading-color">' + selectVariantTranslationText + '</h4></div><div style="display: flex; margin-bottom: 60px; max-width: 100%; flex-wrap: nowrap; overflow-x: scroll;" >');
          
          // Add all variants
          realVariants.forEach((variant, index) => {
            let tagToPush = '';
            const variantTitle = variant?.title;
            const variantId = variant?.id;
            if(index === 0) {
              // handle changed needed for first (initially selected) variant
              tagToPush = '<button class="philyra__popup__variant-selector-selected btn philyra__selector" id="variant-' + variantId?.toString() + '" value=' + variantId + '>' + variantTitle + '</button>';
              // the variant might not be available
              variant.available ? setButtonToAvailable(addToCartBtn) : setButtonToSoldOut(addToCartBtn);
              // the variant might have a different price
              setPrice(variant.price)
            // set value of add to cart button
            assignValueToCartBtn(variantId);
            } else {
              tagToPush = '<button class="philyra__popup__variant-selector btn philyra__selector" id="variant-' + variantId?.toString() + '" value=' + variantId + '>' + variantTitle + '</button>';
            }
            variantsSectionArray.push(tagToPush);
          });
          
          variantsSectionArray.push('</div>');
       }
       
       if(variantsSectionArray?.length){
          variantsSectionHtml = variantsSectionArray.join('');
       }
       
       variantsSection.innerHTML = variantsSectionHtml;
       addEventListenerToVariantButtons();
       addToCartBtn.addEventListener('click', event => {
          handleSubmit(addToCartBtn.value);
       });
    }
    
    const addHoverEventListeners = () => {
        // Get all keywords
        const keywords = document.querySelectorAll('.philyra__blog-keyword');
             keywords.forEach((kw) => {
              kw.addEventListener('mouseover', event => {
                insertProductData(kw.innerHTML);
                kwEventListener();
                registerMouseHover();
              });
             
              kw.addEventListener('click', event => {
                insertProductData(kw.innerHTML);
                kwEventListener();
                registerMouseHover();
              });
             });
    } 
             
    const addEmbedEventListeners = () => {
        const embedButtons = document.querySelectorAll('.philyra__product-embed-button');
             embedButtons.forEach((btn) => {
              btn.addEventListener('click', event => {
                insertProductData(btn.value);
                kwEventListener();
                registerMouseHover();
              });
             });
    }
    
    const handlePageExclude = (excludedPages) => {
        const currentPage = document.getElementById('philyraPageUrl').innerHTML;
        const idx = excludedPages.findIndex((page) => {
            return page === currentPage;
         });
        return idx >= 0;
    }

    const getProductData = async () => {

      for(let i = 0; i < products.length; i++){
        const productHandle = products[i];
        const philyraProductData = await fetch('/products/' + productHandle + '.js');
        const philyraJsonData = await philyraProductData.json();
        productDataStorage[productHandle] = philyraJsonData;
      }
   
      console.log(productDataStorage);
    }
    
    document.addEventListener("DOMContentLoaded", async function(event) { 
       // check for excluded pages here
        const keywords = {"keywords":["Power Luxe"]}.keywords;
        const tags = {"tags":["[POWERLIFT]"]}.tags;
        const excludedPages = {"excludedPages":[]}.excludedPages;
        const isExcluded = handlePageExclude(excludedPages);
        if(!isExcluded){

          if(true) {
            replaceKeywords(keywords); 
          }	
    
          if(true) {
            replaceTags(tags);
          }

          await getProductData();

          replaceProductEmbedImages();

          if(true) {
            addEmbedEventListeners();
          }

          if(true) {
            addHoverEventListeners();
          }	

          addCloseEventListeners();
        }
    });    
      