# PullToRefresh
![](https://github.com/phuhuynh2411/PullToRefresh/blob/master/Pull%20to%20refresh.gif)

Add a Pull to Refresh feature to the table view controller.

## Usage
- Add the following code to the viewDidLoad method of the table view controller
```swift
refreshControl = UIRefreshControl()
refreshControl?.attributedTitle = NSAttributedString(string: "Pull to refresh")
refreshControl?.addTarget(self, action: #selector(refreshTableView(sender:)), for: .valueChanged)
```
- Add a method to refresh the table view data source. You must call the refreshController?.endRefreshing() method at a point in the code to end refresing.
```swift
@objc func refreshTableView(sender: AnyObject){
        print("Refresh the table view")
        refreshControl?.endRefreshing()
}
```
        
