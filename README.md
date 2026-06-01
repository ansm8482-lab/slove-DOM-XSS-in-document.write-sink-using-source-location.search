# slove-DOM-XSS-in-document.write-sink-using-source-location.search
 DOM XSS in document.write sink using source location.search

                        
                        
                        
                 //DOM XSS in document.write sink using source location.search
                        
                        function trackSearch(query) {
                            document.write('<img src="/resources/images/tracker.gif?searchTerms='+query+'">'); //not safe
                            //
                              //safe code


                                 //document.write('<img src="/resources/images/tracker.gif?searchTerms='+encodeURIComponent(query)+'">');
                            
                            
                        }



                        var query = (new URLSearchParams(window.location.search)).get('search');


                        if(query) {
                            trackSearch(query);
                        }


                          //slove the lab
                          //anas" onload="alert(1)
