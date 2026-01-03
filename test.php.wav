<?php
// URL of the remote server (replace with the exact URL or IP)
$remote_url = 'http://10.0.12.12';  // This should be your target IP or URL

// Initialize cURL session
$ch = curl_init();

// Set the URL to the remote server
curl_setopt($ch, CURLOPT_URL, $remote_url);

// Set option to return the transfer as a string
curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);

// Set timeout (e.g., 10 seconds)
curl_setopt($ch, CURLOPT_TIMEOUT, 10);

// Execute the cURL request
$response = curl_exec($ch);

// Get the HTTP status code of the response
$http_code = curl_getinfo($ch, CURLINFO_HTTP_CODE);

// Close the cURL session
curl_close($ch);

// Check if the response is successful or not
if ($http_code == 200) {
    echo "Success: The request was successfully sent to the server.";
} else {
    echo "Failed: Could not reach the server. HTTP Code: " . $http_code;
}

// Optionally, output the response content for debugging
echo "<pre>" . htmlspecialchars($response) . "</pre>";

?>
