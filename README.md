import UIKit
import WebKit

class ViewController: UIViewController {
    override func viewDidLoad() {
        super.viewDidLoad()
        let webView = WKWebView(frame: self.view.frame)
        if let url = Bundle.main.url(forResource: "codecraft", withExtension: "html") {
            webView.loadFileURL(url, allowingReadAccessTo: url)
        }
        self.view.addSubview(webView)
    }
}
