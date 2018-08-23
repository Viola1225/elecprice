#clean function
clean<-function(df){
  # clean raw data
  # rename columns and define types, select columns
  # @return: cleaned dataframe with some columns kept
  
  columns<-c("ID",
             "TDU",
             "REP",
             "PRODUCT",
             "KWH500",
             "KWH1000",
             "KWH2000",
             "FEES",
             "PREPAID",
             "TOU",
             "FIXED",
             "RATE_TYPE",
             "RENEWABLE",
             "TERM_LENGTH",
             "CANCEL_FEE",
             "WEBSITE",
             "TERMS",
             "TERMS_URL",
             "PROMOTION",
             "PROMOTION_DESC",
             "FACTS_URL",
             "ENROLL_URL",
             "PREPAID_URL",
             "ENROLL_PHONE",
             "NEW_CUST",
             "MIN_USAGE_FEE",
             "LANGUAGE",
             "RATING")
  colnames(df)=columns

  df=df %>% #mutate
    select("ID",
           "TDU",
           "REP",
           "PRODUCT",
           "KWH500",
           "KWH1000",
           "KWH2000",
           "RATE_TYPE",
           "RENEWABLE",
           "TERM_LENGTH",
           "PREPAID",
           "TOU",
           "PROMOTION",
           "FACTS_URL") %>%
  mutate(KWH500=KWH500*100,
         KWH1000=KWH1000*100,
         KWH2000=KWH2000*100,
         PREPAID=as.logical(PREPAID),
         TOU=as.logical(TOU),
         PROMOTION=as.logical(PROMOTION)) 
  df=na.omit(df)
  return(df)
}



# get_df<-function(){
#   url<-"http://www.powertochoose.org/en-us/Plan/ExportToCsv"
#   df<-read.csv(file = url,header = TRUE,stringsAsFactors = FALSE)
#   df<-clean(df)
# }

get_df<-function(){
  df<-read.csv(file = "D:\\user\\01378037\\docum\\GitHub\\elecprice\\power-to-choose-offers.csv",header = TRUE,stringsAsFactors = FALSE)
  df<-clean(df)
}


