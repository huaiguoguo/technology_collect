    setInterval(function(){
      const now = Date.parse(new Date())/1000;
      const endTimeStamp = parseInt(_this.lasttime) - now;
      const everyDay = 60*60*24;
      const everyHour = 60*60;
      const everyMinute = 60;
      const day = Math.floor(endTimeStamp/everyDay);
      const hour = Math.floor((endTimeStamp - day*everyDay)/everyHour);
      const minute = Math.floor((endTimeStamp - day*everyDay - hour*everyHour)/everyMinute);
      const second = Math.floor(endTimeStamp - day*everyDay - hour*everyHour - minute*everyMinute);
      _this.lasttimeStr = `${day}天${hour}时${minute}分${second}秒`;
    }, 1000);
