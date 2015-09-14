NSArray * array=[bundle loadNibNamed:@"YJApp" owner:nil options:nil];  

中 LoadNibNamed后面的字符串YJApp一定不要带后缀名，

否则回报错：Terminating app due to uncaught exception 'NSInternalInconsistencyException', reason: 'Could not load NIB in bundle
