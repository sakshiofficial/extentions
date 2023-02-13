
const updateHitsFunction = () => {
   toolTipInitialise();
   hotReloadSim();

   if(JSON.stringify(hitCopy) !== JSON.stringify(hits)){
     clearInterval(reloadingInterval.current)
      updateHitsFunction()
     return 
   }
   reloadingInterval.current = setInterval(() =› { 
      hotReloadSim();
   }, 1000 * process.env.REACT_APP_ HOT_REFRESH INTERVAL);
}


useEffect(()=>{
updateHitsFunction()
return ()=>clearInternval(reloadingInterval.current)
},[hits])
