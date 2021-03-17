# OpenID-Connect-CSharp-Sample-Application
This sample code will help you test openId connect authentication.

Prerequisites

    .NET Core SDK 3.1.
    A text editor or code editor of your choice.
    You already created a Application in your Identity Provider(IDP) and have ClientId, ClientSecret, Authority URL

Configuring the Application

    open ..\OIDCSampleApplication\OIDCSampleApplication\Config\config.json in the text Editor
    Configure ClientId, ClientSecret, Authority
    Ex: "OIDCConfig": { "ClientId": "XXXXXXXX", "ClientSecret": "MySecret", "Authority": "http://{IDP hostname}/auth/realms/{RealmName}" }
    Ex for "Authority": "http://100.123.12.11/auth/realms/MyOIDCRealm"

How To Run

    Navigate to ..\OIDCSampleApplication\OIDCSampleApplication via cmd
    dotnet Build
    dotnet Run
    Application will Start running at some localhost port Ex: http://localhost:55074/
    Copy the Url and Open it in Browser to Authenticate

Alternate way to Run the App

    Install Visual Studio 2017 Community or Professional or Above version
    Open OIDCSampleApplication.sln in the visual Studio
    Run the Application from Visual Studio by pressing F5 key
    Application will open in browser to Authenticate

If Client is Public

    If your Client is public, do not change the Client Secret.
    ClientSecret will be ignored for public client

By Default Sample app is running for Authorization and Implicit flow.
Only Authorization Flow

    By Default Sample app is running for Authorization and Implicit flow.
    If you want the app to be running only in Authorization flow.
    Change the public const string ResponseType = "code id_token"; in Constants.cs
    it should be public const string ResponseType = "code";

Only Implicit Flow

    By Default Sample app is running for Authorization and Implicit flow.
    If you want the app to be running only in Implicit flow.
    Change the public const string ResponseType = "code id_token"; in Constants.cs
    it should be public const string ResponseType = "id_token";

