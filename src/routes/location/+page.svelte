<div id="location-filter">
    <div class="d-flex justify-content-between flex-wrap flex-md-nowrap align-items-center pt-3 pb-2 mb-3 border-bottom">
  
        <div class="btn-toolbar mb-2 mb-md-0">
            <input type="text" id="device" class="form-control" placeholder="id"/>
            <input type="password" id="authorization" class="form-control" placeholder="device authorization code"/>
            <input type="password" id="password" class="form-control" placeholder="password"/>
            <div class="btn-group mr-2">
              <button id="min10" type="button" class="btn btn-sm btn-outline-secondary" onclick="locationui.drawLocations(device.value, 10,password.value, authorization.value)">10분전 위치</button>
              <button id="hour1" type="button" class="btn btn-sm btn-outline-secondary" onclick="locationui.drawLocations(device.value, 60, password.value, authorization.value)">1시간 전 위치</button>
              <button id="hour3" type="button" class="btn btn-sm btn-outline-secondary" onclick="locationui.drawLocations(device.value, 180, password.value, authorization.value)">3시간 전 위치</button>
              <button id="hour6" type="button" class="btn btn-sm btn-outline-secondary" onclick="locationui.drawLocations(device.value, 360, password.value, authorization.value)">6시간 전 위치</button>
              <input id="datetimes" readonly type="text" fromurl="false" name="datetimes" />
              <p id="rangeText"></p>
            </div>
            
          <div class="input-group-addon">
              <span class="glyphicon glyphicon-th"></span>
          </div>
          
          <!-- <div class="form-check form-switch">
            <input class="form-check-input" type="checkbox" id="realtimeLocation">
            <label class="form-check-label" for="realtimeLocation">실시간</label>
          </div> -->
        </div> 
       
      </div>
      <div class="spinner-border" style="width: 3rem; height: 3rem; display: none; position:fixed " id="loading" role="status">
        <span class="sr-only">Loading...</span>
      </div>
      
</div>
<div class="buttons">
  <button id="share" onclick="locationui.share()" type="button" class="btn  btn-sm  btn-outline-secondary ">URL 복사하기(*주의)</button>
  <p>주의: 신뢰할 수 있는 사람에게만 공유하세요. 신뢰하는 사람에게 링크가 공유될 시 본인과 신뢰할 수 있는 사람이 보게 되며, <b>신뢰할 수 있는 분은 또 다른 분에게 공유가 가능하기 때문에, 보내려는 분에겐 보안을 지켜달라고 말해주세요.</b></p>
</div>

<div id="map-area">
    <div id="map"></div>
</div>
<div id="timetable">
  <div id="visualization"></div>
</div>
<div id="detail">
  <code id="debugmessage">
  </code>
</div>