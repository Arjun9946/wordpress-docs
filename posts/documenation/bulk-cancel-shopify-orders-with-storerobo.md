---
title: Bulk Cancel Shopify Orders with StoreRobo
date: 2024-12-13 10:01:00
modified: 2024-12-13 11:47:11
categories:
  - documenation
  - documenation/storerobo/import
  - documenation/storerobo
---


<!-- wp:paragraph -->
<p>Whether you are testing, have a large number of spam orders, or have an inventory shortage, you may want to cancel many orders quickly. While Shopify provides options to cancel orders, canceling orders one by one in Shopify is not easy if you are working with many orders.a</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>With <a href="https://apps.shopify.com/storerobo-import-export-app"><strong>StoreRobo Import Export Suite</strong></a>, you can cancel multiple orders in bulk, saving time and effort.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="Before-you-begin-Shopify-bulk-order-cancellations">Before you begin Shopify bulk order cancellationsa</h2>
<!-- /wp:heading -->

<!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><strong>Double-check</strong> <strong>orders: </strong>Cancellations cannot be undone in Shopify. You would need to recreate canceled orders manually to restore them. Always review the list before confirming cancellations.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Cancel notification: </strong>StoreRobo does not send notifications. You can configure customer notifications while you cancel the orders with the CSV if needed.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Double-check filters</strong>: Use precise filters to ensure you only select orders you want to cancel.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Test small batches</strong>: Start with a small group of orders to confirm the process works as expected.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="Use-Case">Use Case</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>In this tutorial, we’ll demonstrate how to cancel all orders placed by a <strong>specific user(Spam)</strong> after <strong>September 23rd</strong>.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="Bulk-cancel-Shopify-orders">Bulk cancel Shopify orders</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Bulk canceling orders with StoreRobo involves three simple steps:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><strong>Step1: Export Orders to Cancel</strong></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Step2: Mark Orders for Cancellation in CSV / Update columns(</strong><br><code>ID</code><br><code>Name</code><br><code>Cancel: Reason</code><br><code>Cancel: Send Receipt</code><br><code>Cancel: Refund</code><br><strong>)</strong></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Step3: Import Updated Orders into Shopify</strong></li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="Step-1:-Export-Shopify-orders-to-cancel">Step 1: Export Shopify orders to cancel</h2>
<!-- /wp:heading -->

<!-- wp:list {"ordered":true,"start":1} -->
<ol start="1" class="wp-block-list"><!-- wp:list-item -->
<li>Go to <strong>Apps &gt; StoreRobo &gt; Export</strong> in your Shopify admin.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Select an <strong>export template</strong> (e.g., Shopify CSV).</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Choose <strong>Orders</strong> as the data type and configure the export.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:shortcode -->
[wt-info-box icon="👉" theme="primary"]
<!-- /wp:shortcode -->

<!-- wp:paragraph -->
<p><strong>Columns to export for effective order cancellation:</strong></p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><strong>Basic columns:</strong><!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><code>ID</code></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><code>Name</code></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><code>Cancel: Reason</code></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><code>Cancel: Send Receipt</code></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><code>Cancel: Refund</code></li>
<!-- /wp:list-item --></ul>
<!-- /wp:list --></li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Ensure you have selected the specified columns for export. While it may seem that we are only updating the order status to <strong>canceled</strong>, it is important to modify the displayed data for effective order management and proper cancellation of Shopify orders.</p>
<!-- /wp:paragraph -->

<!-- wp:shortcode -->
[/wt-info-box]
<!-- /wp:shortcode -->

<!-- wp:list {"ordered":true,"start":4} -->
<ol start="4" class="wp-block-list"><!-- wp:list-item -->
<li><strong>Apply Filters</strong>: For this example, filter orders placed <strong>after September 23rd</strong> by a user with mail id, <code>johndeo@gmail.com</code></li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:image {"id":638698,"width":"501px","height":"auto","sizeSlug":"large","linkDestination":"none","align":"center"} -->
<figure class="wp-block-image aligncenter size-large is-resized"><img src="https://www.webtoffee.com/wp-content/uploads/2024/12/Export-orders-to-cancel-629x1024.png" alt="Export orders to cancel" class="wp-image-638698" style="width:501px;height:auto"/><figcaption class="wp-element-caption">Export orders to cancel</figcaption></figure>
<!-- /wp:image -->

<!-- wp:list {"ordered":true,"start":4} -->
<ol start="4" class="wp-block-list"><!-- wp:list-item -->
<li>Click <strong>Export</strong> and download the file.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>For more details on exporting orders, refer to the guide <a href="https://www.webtoffee.com/import-export-shopify-orders-with-storerobo/"><strong>Import/Export Shopify Orders with StoreRobo.</strong></a></p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="Step-2:-Update-the-CSV-for-Shopify-orders-cancellation">Step 2: Update the CSV for Shopify orders cancellation</h2>
<!-- /wp:heading -->

<!-- wp:list {"ordered":true,"start":1} -->
<ol start="1" class="wp-block-list"><!-- wp:list-item -->
<li>Open the exported CSV file in a spreadsheet editor.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Delete unnecessary columns or rows(orders), if any.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Update the CSV file as follows:<!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><code>ID</code> ==&gt; No change</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><code>Name</code>==&gt; No Change</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><code>Cancel: Reason</code> ==&gt; Provide reason for order cancellation.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><code>Cancel: Send Receipt</code> ==&gt; Notify the customer of the order cancellation (<strong>YES</strong> to send mail, <strong>NO</strong> to not send)</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><code>Cancel: Refund</code> ==&gt; Set it to <strong>TRUE</strong> to fully refund the order and <strong>FALSE</strong> to not refund.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list --></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Save</strong> the updated CSV file.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:image {"id":638699,"sizeSlug":"large","linkDestination":"none","align":"center"} -->
<figure class="wp-block-image aligncenter size-large"><img src="https://www.webtoffee.com/wp-content/uploads/2024/12/Order-Sample-CSV-Cancel-orders-in-bulk-1024x246.png" alt="Order Sample CSV - Cancel orders in bulk" class="wp-image-638699"/><figcaption class="wp-element-caption">Order Sample CSV - Cancel orders in bulk</figcaption></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2 class="wp-block-heading" id="Step-3:-Import-updated-orders">Step 3: Import updated orders</h2>
<!-- /wp:heading -->

<!-- wp:list {"ordered":true,"start":1} -->
<ol start="1" class="wp-block-list"><!-- wp:list-item -->
<li>Return to the Shopify admin and navigate to <strong>Apps &gt; StoreRobo &gt; Import</strong>.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>Upload</strong> the updated CSV file with Shopify orders to cancel.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Set data type as <strong>Order.</strong></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Click <strong>Proceed</strong>.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Ensure you select the <strong>option to update orders on import</strong>, so existing order statuses are updated to "canceled" instead of creating new orders with that status.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:image {"id":638701,"sizeSlug":"large","linkDestination":"none","align":"center"} -->
<figure class="wp-block-image aligncenter size-large"><img src="https://www.webtoffee.com/wp-content/uploads/2024/12/Update-existing-orders-1-1024x380.png" alt="Update existing orders" class="wp-image-638701"/><figcaption class="wp-element-caption">Update existing orders</figcaption></figure>
<!-- /wp:image -->

<!-- wp:list {"ordered":true,"start":6} -->
<ol start="6" class="wp-block-list"><!-- wp:list-item -->
<li>Click <strong>Import</strong> to begin the process.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>For detailed order import steps, refer to <a href="https://www.webtoffee.com/import-export-shopify-orders-with-storerobo/"><strong>Import/Export Shopify Orders with StoreRobo.</strong></a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>After the import is complete, all selected orders will be marked as canceled in Shopify.</p>
<!-- /wp:paragraph -->

<!-- wp:columns -->
<div class="wp-block-columns"><!-- wp:column -->
<div class="wp-block-column"><!-- wp:image {"id":638703,"sizeSlug":"large","linkDestination":"none","align":"center"} -->
<figure class="wp-block-image aligncenter size-large"><img src="https://www.webtoffee.com/wp-content/uploads/2024/12/Order-before-cancellation-1024x513.png" alt="Orders before cancellation" class="wp-image-638703"/><figcaption class="wp-element-caption">Orders before cancellation</figcaption></figure>
<!-- /wp:image --></div>
<!-- /wp:column -->

<!-- wp:column -->
<div class="wp-block-column"><!-- wp:image {"id":638702,"sizeSlug":"large","linkDestination":"none","align":"center"} -->
<figure class="wp-block-image aligncenter size-large"><img src="https://www.webtoffee.com/wp-content/uploads/2024/12/Orders-after-cancellation-1024x513.png" alt="Orders after cancellation" class="wp-image-638702"/><figcaption class="wp-element-caption">Orders after cancellation</figcaption></figure>
<!-- /wp:image --></div>
<!-- /wp:column --></div>
<!-- /wp:columns -->

<!-- wp:shortcode -->
[wt-info-box icon="📚" theme="primary"]
<!-- /wp:shortcode -->

<!-- wp:paragraph -->
<p><strong>Also read:</strong></p>
<!-- /wp:paragraph -->

<!-- wp:columns -->
<div class="wp-block-columns"><!-- wp:column -->
<div class="wp-block-column"><!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><strong><a href="https://www.webtoffee.com/update-shopify-orders-easily-with-csv-import/">Update Shopify Orders Easily with CSV Import</a></strong></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><a href="https://www.webtoffee.com/archive-and-unarchive-shopify-orders-in-bulk-with-storerobo/">Archive and Unarchive Shopify Orders in Bulk with StoreRobo</a></strong></li>
<!-- /wp:list-item --></ul>
<!-- /wp:list --></div>
<!-- /wp:column -->

<!-- wp:column -->
<div class="wp-block-column"><!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><strong><a href="https://www.webtoffee.com/bulk-update-payment-status-of-shopify-orders-to-paid/">Bulk Update Payment Status of Shopify Orders to Paid</a></strong></li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><a href="https://www.webtoffee.com/how-to-bulk-fulfill-existing-shopify-orders-with-csv/">How to Bulk Fulfill Existing Shopify Orders with CSV</a></strong></li>
<!-- /wp:list-item --></ul>
<!-- /wp:list --></div>
<!-- /wp:column --></div>
<!-- /wp:columns -->

<!-- wp:shortcode -->
[/wt-info-box]
<!-- /wp:shortcode -->