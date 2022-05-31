<!DOCTYPE html>
<!--
To change this license header, choose License Headers in Project Properties.
To change this template file, choose Tools | Templates
and open the template in the editor.
-->
<html lang="en">
    <style>
        * {
            box-sizing: border-box;
        }
        
        #searchInput {
            background-image: url('https://www.w3schools.com/css/searchicon.png');
            background-position: 10px 10px;
            background-repeat: no-repeat;
            width: 100%;
            font-size: 16px;
            padding: 12px 20px 12px 40px;
            border: 1px solid #ddd;
            margin-bottom: 12px;
        }

        body {
            background-color: #f1f1f1;
            padding: 20px;
            font-family: Arial;
        }

        /* Center website */
        .main {
            max-width: 1000px;
            margin: auto;
        }

        h1 {
            font-size: 50px;
            word-break: break-all;
        }

        .row {
            margin: 8px -16px;
        }

        /* Add padding BETWEEN each column (if you want) */
        .row,
        .row > .column {
            padding: 8px;
        }

        /* Create three equal columns that floats next to each other */
        .column {
            float: left;
            width: 25%;
            display: none; /* Hide columns by default */
        }

        /* Clear floats after rows */
        .row:after {
            content: "";
            display: table;
            clear: both;
        }

        /* Content */
        .content {
            background-color: white;
            padding: 10px;
        }

        /* The "show" class is added to the filtered elements */
        .show {
            display: block;
        }

        /* Style the buttons */
        .btn {
            border: none;
            outline: none;
            padding: 12px 16px;
            background-color: white;
            cursor: pointer;
        }

        /* Add a grey background color on mouse-over */
        .btn:hover {
            background-color: #ddd;
        }

        /* Add a dark background color to the active button */
        .btn.active {
            background-color: #666;
            color: white;
        }
        
        /* Style the list and grid buttons */
        .lgbtn {
            border: none;
            outline: none;
            padding: 12px 16px;
            background-color: white;
            cursor: pointer;
            float: right;
        }

        /* Add a grey background color on mouse-over */
        .lgbtn:hover {
            background-color: #ddd;
        }

        /* Add a dark background color to the active button */
        .lgbtn.active {
            background-color: #666;
            color: white;
        }
        
        /*Style of the links for business name and description*/
        a:link {
            text-decoration:none;
            color:black;
        }

        a:visited {
            color: black;
        }
        
        .keywords {
            display: none;
        }
    </style>
  <body>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
      
    <input type="text" id="searchInput" onkeyup="searchFilter()" placeholder="What are you looking for?">
    
    <div id="myBtnContainer">
        <button class="btn active" onclick="filterSelection('all')"> Show all</button>
        <button class="btn" onclick="filterSelection('art')"> Art</button>
        <button class="btn" onclick="filterSelection('classes')"> Classes</button>
        <button class="btn" onclick="filterSelection('fitness')"> Fitness</button>
        <button class="btn" onclick="filterSelection('food and drink')"> Food & Drink</button>
        <button class="btn" onclick="filterSelection('glass')"> Glass</button>
        <button class="btn" onclick="filterSelection('home')"> Home</button>
        <button class="btn" onclick="filterSelection('religion')"> Religion</button>
        <button class="btn" onclick="filterSelection('services')"> Services</button>
        <button class="btn" onclick="filterSelection('shopping')"> Shopping</button>
        <a href="DowntownTiffin_BusinessDatabase_ListView.html">
            <button class="lgbtn"><i class="fa fa-bars"></i> List</button>
        </a>
        <a href="DowntownTiffin_BusinessDatabase_GridView.html">
            <button class="lgbtn"><i class="fa fa-th-large"></i> Grid</button>
        </a>
    </div>

    <!-- Portfolio Gallery Grid -->
    <div class="row" id="myPortfolio">
        <div class="column services">
            <div class="content" data-keywords="salon, hair, makeup, tanning, haircuts, haircolor, downtown, tiffin, waxing, facials, skin care, stylists, nails, manicure, bridal">
                <a href="BusinessHTMLs/AirbrushBeauty.html">
                    <img src="BusinessPictures/AirbrushBeauty_cut.png" alt="Airbrush Beauty Logo" style="width:100%">
                    <h4>Airbrush Beauty</h4>
                    <p>Airbrush beauty is a full service salon located next to the barber shop and jolly's on market st. We specialize in bridal services as well as premium hair, skin, and nail care. We offer makeup...</p>
                </a>
            </div>
        </div>
        <div class="column home">
            <div class="content" data-keywords="appliances, home improvement">
                <a href="BusinessHTMLs/BurnsElectric.html">
                    <img src="BusinessPictures/BurnsElectric_cut.png" alt="Burns Electric Logo" style="width:100%">
                    <h4>Burns Electric</h4>
                    <p>Lighting and appliances showroom, kitchen and lighting design center, flooring, counter tops and back splashes, lamp shades and much more!</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="salon, men's haircut, women's haircut, barbershop">
                <a href="BusinessHTMLs/Champs.html">
                    <img src="BusinessPictures/Champs_cut.png" alt="Champs Logo" style="width:100%">
                    <h4>Champs Barber Shop</h4>
                    <p>Champs Barber Shop is a 4 chair shop with all walk ins. Our hours are Monday-Friday 8:30am-6:00pm and Saturday 7:00am-1:00pm. We are located downtown Tiffin between Clover Club and Uncle Mike's.</p>
                </a>
            </div>
        </div>
        <div class="column food and drink">
            <div class="content" data-keywords="">
                <a href="BusinessHTMLs/CloverClub.html">
                    <img src="BusinessPictures/CloverClub_cut.png" alt="Clover Club Logo" style="width:100%">
                    <h4>Clover Club</h4>
                    <p>Take a breather from your busy schedule and spend quality time with your family and friends. Turn to the Clover Club Tavern & Eatery in Tiffin, OH if you are looking for a perfect place to hang out...</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column services">
            <div class="content" data-keywords="travel, events, destination weddings, honeymoons">
                <a href="BusinessHTMLs/DanaBraun.html">
                    <img src="BusinessPictures/DanaBraun_cut.png" alt="Dana Braun Logo" style="width:100%">
                    <h4>Dana Braun Travel Design, LLC</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="auto insurance, homeowners insurance, life insurance">
                <a href="BusinessHTMLs/EdHanley.html">
                    <img src="BusinessPictures/EdHanley_cut.png" alt="Ed Hanley Logo" style="width:100%">
                    <h4>Ed Hanley Agency, State Farm Insurance</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="help, seniors, assistance, information, food, shelter, homeless, rent, christmas, school supplies">
                <a href="BusinessHTMLs/FirstCall.html">
                    <img src="BusinessPictures/FirstCall_cut.png" alt="First Call Logo" style="width:100%">
                    <h4>First Call for Help</h4>
                    <p>First Call For Help is a service of Tiffin-Seneca United Way that gives direct assistance to the people of Tiffin and Seneca County. The primary mission of First Call For Help is to provide...</p>
                </a>
            </div>
        </div>
        <div class="column food and drink">
            <div class="content" data-keywords="">
                <a href="BusinessHTMLs/FortBall.html">
                    <img src="BusinessPictures/FortBall_cut.png" alt="Fortball Logo" style="width:100%">
                    <h4>Fort Ball Pizza Palace - Melmore St</h4>
                    <p>Fort Ball Pizza Palace is the biggest buffet in TIffin, with a mouthwatering variety of Italian food you will find something to satisfy everyone's taste. See you soon!</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column food and drink">
            <div class="content" data-keywords="">
                <a href="BusinessHTMLs/FortBall.html">
                    <img src="BusinessPictures/FortBall_cut.png" alt="Fortball Logo" style="width:100%">
                    <h4>Fort Ball Pizza Palace - Washington St</h4>
                    <p>Fort Ball Pizza Palace is the biggest buffet in TIffin, with a mouthwatering variety of Italian food you will find something to satisfy everyone's taste. See you soon!</p>
                </a>
            </div>
        </div>
        <div class="column food and drink">
            <div class="content" data-keywords="frozen yogurt, dessert, ice cream, yogurt, toppings, family-owned, gift cards, laird building, chocolate, frozone, boba balls, hot chocolate fudge, dessert, sweet treats, toppings, food, yogurt">
                <a href="BusinessHTMLs/Frozone.html">
                    <img src="BusinessPictures/Frozone_cut.png" alt="Frozone Logo" style="width:100%">
                    <h4>FroZone Frozen Yogurt</h4>
                    <p>FroZone is a family owned frozen yogurt shop in downtown Tiffin offering 12 different yogurt / sorbet flavors and over 30 fun toppings. Come in and create your own unique masterpiece!</p>
                </a>
            </div>
        </div>
        <div class="column classes fitness">
            <div class="content" data-keywords="yoga, massage, meditation, wellness, reflexology, reiki, raniosacral, aromatherapy, essential oils, therapeutic yoga, healing, stress relief, energy work, community outreach">
                <a href="BusinessHTMLs/GemYoga.html">
                    <img src="BusinessPictures/GemYoga_cut.png" alt="Gem Yoga Logo" style="width:100%">
                    <h4>Gem Yoga and Life Enrichment</h4>
                    <p>Established in 2014, Gem Yoga and Life Enrichment became Tiffin's first studio dedicated to the practice of yoga. Since then, we have grown into a center which focuses on cultivating well-being...</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="salon, haircut, hair color, wax, extensions">
                <a href="BusinessHTMLs/HairStudio47.html">
                    <img src="BusinessPictures/HairStudio47_cut.png" alt="Hair Studio 47 Logo" style="width:100%">
                    <h4>Hair Studio 47</h4>
                    <p></p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column glass shopping">
            <div class="content" data-keywords="gifts, crystal, barware, glassware, ornaments, awards, wedding, bourbon glass, wine glass, martini glass, decanter, window, crystal repair, champagne glass, vases, crystal bowl, customized, personalized, etching, engrave, beer can glasses, groomsman gifts, bridal gifts, anniversary gifts, birthday gifts, aidan scully, lovebirds, hawkes crystal">
                <a href="BusinessHTMLs/HawkesCrystal.html">
                    <img src="BusinessPictures/HawkesCrystal_cut.png" alt="Hawkes Crystal Logo" style="width:100%">
                    <h4>Hawkes Crystal</h4>
                    <p>Hand-cut glass and crystal pieces, customizable and personalized, for gifts, interior design, architectural design and more!</p>
                </a>
            </div>
        </div>
        <div class="column shopping">
            <div class="content" data-keywords="metaphysical, healing crystal, smudging items, spiritual novelties, art gallery, custom jewelry, handmade jewelry, tarot, reiki healing, oracle, psychic medium, numerology, palmistry, palm readings">
                <a href="BusinessHTMLs/HealingVines.html">
                    <img src="BusinessPictures/HealingVines_cut.png" alt="Healing Vines Logo" style="width:100%">
                    <h4>Healing Vines</h4>
                    <p>Our beautiful metaphysical store is filled with spiritual novelties, healing crystals and an art Gallery. The services we offer are Reiki Sessions, Oracle Readings, Palmistry and numerology readings.</p>
                </a>
            </div>
        </div>
        <div class="column services shopping">
            <div class="content" data-keywords="water, salt, water treatment">
                <a href="BusinessHTMLs/HempyWater.html">
                    <img src="BusinessPictures/HempyWater_cut.png" alt="Hempy Water Logo" style="width:100%">
                    <h4>Hempy Water</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="personal injury, wrongful death, estate planning, probate, real estate, landlord-tenant relationships, business representation, business collections, employee/human resource issues, contract reviews and negotiations, compliance reviews">
                <a href="BusinessHTMLs/LGRC.html">
                    <img src="BusinessPictures/LGRC_cut.png" alt="LGRC Logo" style="width:100%">
                    <h4>Lange Gordon Rannigan & Claus</h4>
                    <p>Whether you're selling or buying a business, planning your estate, settling an estate, or looking for help after you or your loved ones have been hurt in an accident, we offer the expertise and...</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column food and drink">
            <div class="content" data-keywords="bar, restaurant, pub, beer, draft, friendly, service, chicken, burgers, salads, wraps, quesadillas">
                <a href="BusinessHTMLs/MST.html">
                    <img src="BusinessPictures/MST_cut.png" alt="MST Logo" style="width:100%">
                    <h4>MST Pub and Grub</h4>
                    <p>MST offers a wide range of food options including fresh burgers, salads, quesadillas, and our famous chicken chunks. We offer 12 beers on tap which includes our local breweries and some craft...</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="checking accounts, savings accounts, mortgage loans, commercial lending, personal loans, auto loans">
                <a href="BusinessHTMLs/OldFort.html">
                    <img src="BusinessPictures/OldFort_cut.png" alt="Old Fort Logo" style="width:100%">
                    <h4>Old Fort Banking Company</h4>
                    <p>We offer an ATM in Downtown Tiffin for all your shopping needs. Old Fort Banking Company has been serving the greater Tiffin area and community for over 100 years! Stop in and experience the...</p>
                </a>
            </div>
        </div>
        <div class="column religion">
            <div class="content" data-keywords="worship, ministry, young adults, college students">
                <a href="BusinessHTMLs/Overflow.html">
                    <img src="BusinessPictures/Overflow_cut.png" alt="Overflow Ministries Logo" style="width:100%">
                    <h4>Overflow Ministires of Tiffin</h4>
                    <p>The mission of Overflow Ministries of Tiffin (Overflow) is to develop future leaders of the church. Young adults in the area and from Tiffin University and Heidelberg University lead worship...</p>
                </a>
            </div>
        </div>
        <div class="column fitness">
            <div class="content" data-keywords="karate, fitness, martial arts, health, discipline, focus, confidence">
                <a href="BusinessHTMLs/PaksKarate.html">
                    <img src="BusinessPictures/PaksKarate_cut.png" alt="Pak's Karate Logo" style="width:100%">
                    <h4>Pak's Karate</h4>
                    <p>We offer Tang Soo Do Karate classes for all ages. We are very family-oriented and strive to teach values such as self discipline, confidence, and respect.</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column shopping home">
            <div class="content" data-keywords="gifts, appliances, coffee">
                <a href="BusinessHTMLs/Ralphs.html">
                    <img src="BusinessPictures/Ralphs_cut.png" alt="Ralph's Joy of Living Logo" style="width:100%">
                    <h4>Ralph's Joy of Living</h4>
                    <p>There's a reason why our family owned business has been serving this area since 1950 - it's customer satisfaction. Ralph's Joy of Living was built on Ralph's entrepreneurial spirit for appliances, ...</p>
                </a>
            </div>
        </div>
        <div class="column shopping home">
            <div class="content" data-keywords="upcycle, recycle, reclaimed, thrift store, nonprofit, vintage, reloved, refurbished, donation drop off, local retail">
                <a href="BusinessHTMLs/ReclaimIt.html">
                    <img src="BusinessPictures/ReclaimIt_cut.png" alt="ReclaimIt Logo" style="width:100%">
                    <h4>Reclaim It</h4>
                    <p>Reclaim It, in the center of Tiffin, OH's downtown historic district, is a retail store like no other. Curated refurbished vintage furniture and accessories, a broad selection of art from local and...</p>
                </a>
            </div>
        </div>
        <div class="column fitness classes">
            <div class="content" data-keywords="fitness, exercise, classes, workout, barre, ballet, zumba, yoga, personal training">
                <a href="BusinessHTMLs/Releve.html">
                    <img src="BusinessPictures/Releve_cut.png" alt="Releve Logo" style="width:100%">
                    <h4>Relev&eacute; Barre Studio</h4>
                    <p>Relev&eacute; is a boutique fitness featuring adult barre fitness and ballet classes.</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="">
                <a href="BusinessHTMLs/Reser.html">
                    <img src="BusinessPictures/Reser_cut.png" alt="Reser Logo" style="width:100%">
                    <h4>Reser Chiropractic and Perry Spine and Wellness Center</h4>
                    <p>Located at 14 W Market St, on the scenic Sandusky River, Reser Chiropractic and Perry Spine and Wellness Center offer complete chiropractic healthcare for the entire family. This chiropractic...</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column classes">
            <div class="content" data-keywords="classes, workshops, birthday parties, bachelorette parties, DIY projects, wood signs, painting, home décor, arts & crafts, yard signs, girls night out, what to do, room rental, art studio">
                <a href="BusinessHTMLs/RusticFlair.html">
                    <img src="BusinessPictures/RusticFlair_cut.png" alt="Rustic Flair & Brush Logo" style="width:100%">
                    <h4>Rustic Flair &AMP; Brush</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="signs, banners, decals, vehicle wraps">
                <a href="BusinessHTMLs/SamedaySigns.html">
                    <img src="BusinessPictures/SamedaySigns_cut.png" alt="Sameday Signs Logo" style="width:100%">
                    <h4>Sameday Signs</h4>
                    <p>Full sign shop specializing in printing of all kinds. Commercial & noncommercial, walk in welcome.</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="">
                <a href="BusinessHTMLs/SaullLaw.html">
                    <img src="BusinessPictures/SaullLaw_cut.png" alt="Saull Law Logo" style="width:100%">
                    <h4>Saull Law Offices</h4>
                    <p>Welcome to Saull Law & Title, a law firm headquartered in Upper Sandusky, Ohio with offices in Carey, Ohio, Tiffin, Ohio and a satellite office in Bucyrus, Ohio. We have made it our mission to...</p>
                </a>
            </div>
        </div>
        <div class="column shopping">
            <div class="content" data-keywords="gifts, custom gifts, home décor, women&#39;s clothing, jewelry, chocolate">
                <a href="BusinessHTMLs/SimplySusans.html">
                    <img src="BusinessPictures/SimplySusans_cut.png" alt="Simply Susan's Logo" style="width:100%">
                    <h4>Simply Susan's</h4>
                    <p>Find the perfect gift, farmhouse d&eacute;cor, as well as quality clothing, jewelry, and accessories. Hand dipped chocolates, personalized d&eacute;cor and more.</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column religion">
            <div class="content" data-keywords="">
                <a href="BusinessHTMLs/StPauls.html">
                    <img src="BusinessPictures/StPauls_cut.png" alt="St. Paul's Logo" style="width:100%">
                    <h4>St. Paul's United Methodist Church</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="tanning services">
                <a href="BusinessHTMLs/TanItAll.html">
                    <img src="BusinessPictures/TanItAll_cut.png" alt="Tan It All Logo" style="width:100%">
                    <h4>Tan It All</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column shopping">
            <div class="content" data-keywords="children, consignment store, school uniforms">
                <a href="BusinessHTMLs/TheBeanstalk.html">
                    <img src="BusinessPictures/TheBeanstalk_cut.png" alt="The Bean Stalk Logo" style="width:100%">
                    <h4>The Beanstalk, LLC</h4>
                    <p>Consignment store. Sells gently used clothes and accessories from newborn to 10-12 kids. We also sell new & used school uniforms.</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="venue, banquet hall, wedding, reception, bar, caterer, catering, event space">
                <a href="BusinessHTMLs/TheChandelier.html">
                    <img src="BusinessPictures/TheChandelier_cut.png" alt="The Chandelier Logo" style="width:100%">
                    <h4>The Chandelier Community Events Center</h4>
                    <p>A full service event venue located in historic downtown Tiffin. Our location provides a premier setting for large or small events of any kind, able to accommodate over 400 guests. We offer catering...</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column food and drink">
            <div class="content" data-keywords="brewery, beer, t-shirt, hat, sticker, keychain, taproom, seltzer, cider, mug, tag-a-brew, stein, beaker, flight, music, trivia, craft beer, ocba, ba, growler, bottle, can, crowler, howler, whiskey stix, ballreichs, keg, pretzels, potato chips, gift certificate, membership, merchandise, happy hour">
                <a href="BusinessHTMLs/LAB.html">
                    <img src="BusinessPictures/LAB_cut.png" alt="The LAB Logo" style="width:100%">
                    <h4>The Laird Arcade Brewery</h4>
                    <p>We are a 3.5 BBL brewhouse focusing mostly on taproom sales, with some local distribution. Our emphasis is to promote as much local business as we can. We strive to keep our ingredients as locally...</p>
                </a>
            </div>
        </div>
        <div class="column food and drink">
            <div class="content" data-keywords="craft cocktails, draft beer, wine, fine dining, live music, steaks, seafood, homemade desserts, upscale">
                <a href="BusinessHTMLs/TheEmpire.html">
                    <img src="BusinessPictures/TheEmpire_cut.png" alt="The Empire Logo" style="width:100%">
                    <h4>The Empire at 138</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column food and drink">
            <div class="content" data-keywords="bar, bourbon, cocktails, cigars, live music, food truck, limousine services, party bus, wine tours, brewery tours, greek food, grilled sandwiches, party room, wedding transportation, gyro, gyro salad, beer, wine, whiskey">
                <a href="BusinessHTMLs/TheRenaissance.html">
                    <img src="BusinessPictures/TheRenaissance_cut.png" alt="The Renaissance Logo" style="width:100%">
                    <h4>The Renaissance of Tiffin (Pink Lady Food Truck & Party Bus)</h4>
                    <p>A roarin' 1920's themed bar located in Tiffin's Historic Downtown. Featuring 336 liquors and timeless cocktails.</p>
                </a>
            </div>
        </div>
        <div class="column art">
            <div class="content" data-keywords="music, theatre, dance, concerts, theater, shows, stage, rental, comedy, piano, historic, vaudeville, movies, country, pop, classical, ritz, national, tickets, performing, arts, players">
                <a href="BusinessHTMLs/Ritz.html">
                    <img src="BusinessPictures/Ritz_cut.png" alt="Ritz Theatre Logo" style="width:100%">
                    <h4>The Ritz Theatre</h4>
                    <p>This historic 1928 vaudeville era theatre was renovated in 1998. The Ritz serves the Northwest Ohio region as a leading performing arts center hosting national headliners, music, touring...</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column services">
            <div class="content" data-keywords="beauty salon, beauty school, classes, education, cosmetology, college, nails, hairstyling services">
                <a href="BusinessHTMLs/TiffinAcademy.html">
                    <img src="BusinessPictures/TiffinAcademy_cut.png" alt="Tiffin Academy Logo" style="width:100%">
                    <h4>Tiffin Academy of Hair Design</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column art">
            <div class="content" data-keywords="art classes, classes, volunteer opportunity, gallery, art gallery, art exhibitions, gift shop, art contests, art festival, classes for children, tag, art, gallery, gifts, exhibitions, shows, downtown, tiffin">
                <a href="BusinessHTMLs/TAG.html">
                    <img src="BusinessPictures/TAG_cut.png" alt="TAG Logo" style="width:100%">
                    <h4>Tiffin Art Guild & Gallery</h4>
                    <p>The Tiffin Art Guild has on-going art exhibits of member and guest artwork such as oil, acrylic & watercolor paintings, photography, jewelry, glass and wood sculpture and more. Most of which is for...</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="philanthropy, legacy giving">
                <a href="BusinessHTMLs/TCF.html">
                    <img src="BusinessPictures/TCF_cut.png" alt="TCF Logo" style="width:100%">
                    <h4>Tiffin Community Foundation</h4>
                    <p>The local Community Foundation supporting 501&#169;(3) non-profit organizations in Seneca County.</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="community organizations, scholarship services, social service organizations, veterans & military organizations, youth organizations & centers">
                <a href="BusinessHTMLs/Elks.html">
                    <img src="BusinessPictures/Elks_cut.png" alt="Tiffin Elks Logo" style="width:100%">
                    <h4>Tiffin Elks</h4>
                    <p>Instituted on July 11, 1888, the current building was opened in 1898. The Tiffin Elks occupies the tenth oldest lodge built exclusively as an Elk's lodge. Our lodge is known for our unique Elk's...</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column art glass">
            <div class="content" data-keywords="fine tiffin crystal, decorative glass, antiques, glass books, glass history">
                <a href="BusinessHTMLs/TiffinGlassMuseum.html">
                    <img src="BusinessPictures/TiffinGlassMuseum_cut.png" alt="Tiffin Glass Museum Logo" style="width:100%">
                    <h4>Tiffin Glass Museum & Shoppe</h4>
                    <p>Large display of glass made in Tiffin from 1889 to 1980. Shoppe has for sale many of the same pieces of glass.</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="help, volunteer, community service, information, food, shelter, homeless, rent, agency, pillar, donation, nonprofit, local">
                <a href="BusinessHTMLs/UnitedWay.html">
                    <img src="BusinessPictures/UnitedWay_cut.png" alt="United Way Logo" style="width:100%">
                    <h4>Tiffin-Seneca United Way</h4>
                    <p>Tiffin-Seneca United Way has been the foundation for community success in the areas of health, education, financial, and safety net services. We are in the business of making connections and...</p>
                </a>
            </div>
        </div>
        <div class="column fitness">
            <div class="content" data-keywords="martial arts, self-defense, strength, conditioning">
                <a href="BusinessHTMLs/TracysKarate.html">
                    <img src="BusinessPictures/TracysKarate_cut.png" alt="Tracy's Karate Logo" style="width:100%">
                    <h4>Tracy's Karate Studio</h4>
                    <p></p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="funeral, cremation, burial, pet cremation, casket, urn, embalming, vault">
                <a href="BusinessHTMLs/Traunero.html">
                    <img src="BusinessPictures/Traunero_cut.png" alt="Traunero Logo" style="width:100%">
                    <h4>Traunero Funeral Home and Crematory</h4>
                    <p>Started in 1900 as the Ewald and Pahl Furniture and Undertaking Company. In 1997 the funeral home became Traunero Funeral Home with Richard and Andrea Traunero as owners. In 2010, the Seneca County...</p>
                </a>
            </div>
        </div>
        
        <div style="clear: both;"></div>
        
        <div class="column services">
            <div class="content" data-keywords="insurance, benefits, health insurance, auto insurance, home insurance, life insurance, group insurance, business insurance, investments, locally owned, financial services">
                <a href="BusinessHTMLs/UIS.html">
                    <img src="BusinessPictures/UIS_cut.png" alt="UIS Logo" style="width:100%">
                    <h4>UIS Insurance & Investments</h4>
                    <p>UIS Insurance & Investments is an independent regional insurance agency dedicated to providing our clients with incredible responsive customer service and reliable professional advice.</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="legal services, law, patents, trademarks, copyrights, lawyer, attorney">
                <a href="BusinessHTMLs/WardLaw.html">
                    <img src="BusinessPictures/WardLaw_cut.png" alt="Ward Law Logo" style="width:100%">
                    <h4>Ward Law Office</h4>
                    <p>Law firm specializing in the practice of patent and trademark law. We do not charge for initial consultations.</p>
                </a>
            </div>
        </div>
        <div class="column services">
            <div class="content" data-keywords="wttf, bas broadcasting, 419 day, local business, downtown tiffin, news, sports, announcements, delays, closings, covid updates, what's happening, on the air, community, local">
                <a href="BusinessHTMLs/WTTF.html">
                    <img src="BusinessPictures/WTTF_cut.png" alt="WTTF Logo" style="width:100%">
                    <h4>WTTF 93.3 FM & BAS Broadcasting</h4>
                    <p>WTTF is your hometown radio station located in downtown Tiffin, bringing you the latest news, sports and family-friendly entertainment. Look to WTTF for any of your marketing needs like special...</p>
                </a>
            </div>
        </div>
<!-- END GRID -->
</div>
    <script>
        function searchFilter() {
            //overbusbox is used to control whether the busbox is displayed or not, as we cannot specify display in the busbox itself (we insert "show" into column class name, not content class name)
            var portfolio, busbox, overbusbox, input, keywords;
            portfolio = document.getElementById("myPortfolio");
            busbox = document.getElementsByClassName("content");
            overbusbox = document.getElementsByClassName("column");
            input = document.getElementById("searchInput");
            input = input.value.toLowerCase();
            // Add the "show" class (display:block) to the filtered elements, and remove the "show" class from the elements that are not selected
            for (i = 0; i < busbox.length; i++) {
                keywords = busbox[i].getAttribute("data-keywords");
                //remove all busboxes
                w3RemoveClass(overbusbox[i], "show")
                //only add busboxes with keywords
                if (keywords.toLowerCase().includes(input)) {
                    w3AddClass(overbusbox[i], "show")
                }
            }
        }
        
        filterSelection("all") // Execute the function and show all columns
        function filterSelection(c) {
            var overbusbox, i;
            overbusbox = document.getElementsByClassName("column");
            if (c == "all") {
                c = "";
            }
            // Add the "show" class (display:block) to the filtered elements, and remove the "show" class from the elements that are not selected
            for (i = 0; i < overbusbox.length; i++) {
                w3RemoveClass(overbusbox[i], "show");
                if (overbusbox[i].className.indexOf(c) > -1) {
                    w3AddClass(overbusbox[i], "show");
                }
            }
        }

        // Show filtered elements
        function w3AddClass(element, name) {
            var i, arr1, arr2;
            arr1 = element.className.split(" ");
            arr2 = name.split(" ");
            for (i = 0; i < arr2.length; i++) {
                if (arr1.indexOf(arr2[i]) == -1) {
                    element.className += " " + arr2[i];
                }
            }
        }

        // Hide elements that are not selected
        function w3RemoveClass(element, name) {
            var i, arr1, arr2;
            arr1 = element.className.split(" ");
            arr2 = name.split(" ");
            for (i = 0; i < arr2.length; i++) {
                while (arr1.indexOf(arr2[i]) > -1) {
                    arr1.splice(arr1.indexOf(arr2[i]), 1);
                }
            }
            element.className = arr1.join(" ");
        }

        // Add active class to the current button (highlight it)
        var btnContainer = document.getElementById("myBtnContainer");
        var btns = btnContainer.getElementsByClassName("btn");
        for (var i = 0; i < btns.length; i++) {
            btns[i].addEventListener("click", function(){
                var current = document.getElementsByClassName("active");
                current[0].className = current[0].className.replace(" active", "");
                this.className += " active";
            });
        }
    </script>
    </body>
</html>
