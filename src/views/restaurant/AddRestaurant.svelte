<script>
// core components
// import TableDropdown from "components/Dropdowns/TableDropdown.svelte";
import {
    link
} from "svelte-routing";
let foodtype = "";
// can be one of light or dark
export let color = "light";
</script>

<div class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded {color === 'light' ? 'bg-white' : 'bg-red-800 text-white'}" >
    <div class="block w-full overflow-x-auto">
        <!-- Restaurant info -->
        <div class="col-sm-12 col-lg-12 mb-3 mb-lg-2">
           <form>
            <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase" style="margin-left: 2%;">
              Restaurant Information
            </h6>
            <div class="flex flex-wrap">
              <div class="w-full lg:w-6/12 px-4">
                <div class="relative w-full mb-3">
                  <label
                    class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                    for="restaurantname"
                  >
                    Restaurant Name
                  </label>
                  <input
                    id="restaurantname"
                    type="text"
                    class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                    value=""
                    placeholder="Restaurant Name"
                  />
                </div>
              </div>
            <!-- </div>
            <div class="flex flex-wrap"> -->
             <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="restaurantadd"
                >
                  Restaurant Address
                </label>
                <textarea
                  id="restaurantadd"
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value=""
                  placeholder="Restaurant Address"
                />
              </div>
             </div>
           <!-- </div>
           <div class="flex flex-wrap"> -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="tax"
                >
                  VAT-TAX(%)
                </label>
                <input
                  id="tax"
                  type="number"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="VAT/TAX"
                  min="0"
                  step=".01"
                  required="" 
                  value=""
                />
              </div>
            </div>
          <!-- </div>
          <div class="flex flex-wrap"> -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="charge"
                >
                  Delivery charge(₹)
                </label>
                <input
                  id="charge"
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="10"
                />
              </div>
            </div>
          <!-- </div>
          <div class="flex flex-wrap"> -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="minimum_delivery_time"
                >
                Minimum delivery time (Minutes)
                </label>
                <input
                  id="minimum_delivery_time"
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value=""
                  placeholder="30"
                />
              </div>
            </div>
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="maximum_delivery_time"
                >
                Maximum delivery time (Minutes)
                </label>
                <input
                  id="maximum_delivery_time"
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value=""
                  placeholder="40"
                />
              </div>
            </div>
          <!-- </div>
          <div class="flex flex-wrap"> -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="opening_time"
                >
                Opening time 
                </label>
                <input
                  id="opening_time"
                  type="time"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value=""
                />
              </div>
            </div>
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="maximum_delivery_time"
                >
                Closing time 
                </label>
                <input
                  id="closing_time"
                  type="time"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value=""/>
              </div>
            </div>
          <!-- </div> -->
          <div class="w-full lg:w-6/12 px-4">
            <div class="relative w-full mb-3">
              <label
                class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                for="logo">
                Restaurant Logo
              <small style="color: red"> ( Ratio 1:1 )</small>
              </label>
              <input
                id="logo"
                type="file"
                class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                value=""
                placeholder="Choose File"
                accept=".jpg, .png, .jpeg, .gif, .bmp, .tif, .tiff|image/*"
              />
            </div>
            <br>
            <div class="relative w-full mb-3">
              <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                >
                Food Type
                </label>
              <label>
                <input type=radio bind:group={foodtype} value={1}>
                VEG
              </label>
              
              <label>
                <input type=radio bind:group={foodtype} value={2}>
                NON-VEG
              </label>
              
              <label>
                <input type=radio bind:group={foodtype} value={3}>
                BOTH
              </label>
            </div>
          </div>
          <div class="w-full lg:w-6/12 px-4">
            <center>
<img style="height: 200px;border: 1px solid; border-radius: 10px;" id="viewer" src="https://demo.6amtech.com/stackfood/public/assets/admin/img/400x400/img2.jpg" alt="delivery-man image">
</center>
          </div>
          <!-- <div class="flex flex-wrap"> -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="latitude"
                >
                Latitude
                </label>
                <input
                  id="latitude"
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value=""
                  placeholder="Ex : -94.22213"
                />
              </div>
            </div>
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="longitude"
                >
                Longitude
                </label>
                <input
                  id="longitude"
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value=""
                  placeholder="Ex : 106.22513"/>
              </div>
            </div>
            
            <div style="width: 100%"><iframe width="50%" height="80%" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=en&amp;q=gujarat%20university+(book%20my%20dine)&amp;t=&amp;z=13&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"><a href="https://www.gps.ie/sport-gps/">fitness tracker</a></iframe></div>
          </div>
         
          <!-- <div class="flex flex-wrap"> -->
            <!-- <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="logo">
                  Restaurant Logo
                <small style="color: red"> ( Ratio 1:1 )</small>
                </label>
                <input
                  id="logo"
                  type="file"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value=""
                  placeholder="Choose File"
                  accept=".jpg, .png, .jpeg, .gif, .bmp, .tif, .tiff|image/*"
                />
              </div>
            </div> -->
          <!-- </div> -->
          
            
            <hr class="mt-6 border-b-1 border-blueGray-300" />

              <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase" style="margin-left: 2%;">
                Owner Information
              </h6>
              <div class="flex flex-wrap">
                <div class="w-full lg:w-4/12 px-4">
                  <div class="relative w-full mb-3">
                    <label
                      class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                      for="firstname"
                    >
                      First Name
                    </label>
                    <input
                      id="firstname"
                      type="text"
                      class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                      value=""
                      placeholder="First Name"
                    />
                  </div>
                </div>
                <div class="w-full lg:w-4/12 px-4">
                  <div class="relative w-full mb-3">
                    <label
                      class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                      for="lastname"
                    >
                      Last Name
                    </label>
                    <input
                      id="lastname"
                      type="text"
                      class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                      value=""
                      placeholder="Last Name"
                    />
                  </div>
                </div>
                <div class="w-full lg:w-4/12 px-4">
                  <div class="relative w-full mb-3">
                    <label
                      class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                      for="phone"
                    >
                      Phone
                    </label>
                    <input
                      id="phone"
                      type="tel"
                      class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                      value=""
                      placeholder="Phone"
                    />
                  </div>
                </div>
              </div>
        
              <hr class="mt-6 border-b-1 border-blueGray-300" />
        
              <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase" style="margin-left: 2%;">
                Login Information
              </h6>
              <div class="flex flex-wrap">
                <div class="w-full lg:w-4/12 px-4">
                  <div class="relative w-full mb-3">
                    <label
                      class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                      for="email"
                    >
                      Email
                    </label>
                    <input
                      id="email"
                      type="email"
                      class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                      value=""
                      placeholder="EX- example@gmal.com"
                    />
                  </div>
                </div>
                <div class="w-full lg:w-4/12 px-4">
                  <div class="relative w-full mb-3">
                    <label
                      class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                      for="password"
                    >
                      Password
                    </label>
                    <input
                      id="password"
                      type="password"
                      class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                      value=""
                      placeholder="6+ character reqired"
                    />
                  </div>
                </div>
                <div class="w-full lg:w-4/12 px-4">
                  <div class="relative w-full mb-3">
                    <label
                      class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                      for="confirmpassword"
                    >
                      Confirm Password
                    </label>
                    <input
                      id="confirmpassword"
                      type="password"
                      class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                      value=""
                      placeholder="6+ character reqired"
                    />
                  </div>
                </div>
              </div>
              <hr class="mt-6 border-b-1 border-blueGray-300" />

              <div class="flex flex-wrap">
                <div class="w-full lg:w-12/12 px-4" style="margin-block: 2%;">
                  <div class="relative w-full mb-3">
                    <a 
                     use:link
                     href="/restaurant/addrestaurant" 
                     class="bg-red-400 text-white  active:bg-red-500 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150" style="margin-left:2%;">          
                     SUBMIT
                    </a>
                    <!-- <a 
                     use:link
                     href="/restaurant/addrestaurant" 
                     class="bg-red-400 text-white  active:bg-red-500 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150" style="margin-left:3%;">          
                     CANCLE
                    </a> -->
                  </div>
                </div>
              </div>
            </form>
        </div>
    </div>
</div>
