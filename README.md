<!DOCTYPE html>
<html>

<head>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://libs.zappar.com/zappar-aframe/2.0.0/zappar-aframe.js"></script>

    <meta charset="utf-8" />
    <title>Zappar for A-Frame: Face Tracking Face Mesh Example</title>
    <style>
        html,
        body {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
        }
    </style>
</head>

<body>
    <a-scene>
        <!-- Ask user for camera permissions, display some text if permission is denied -->
        <a-entity zappar-permissions-ui id="permissions"></a-entity>
        <!-- shows a full-page dialog that informs the user they're using an unsupported browser -->
        <a-entity zappar-compatibility-ui id="compatibility"></a-entity>

        <a-camera zappar-camera="user-facing: true;" />

        <!-- Setup our instant tracker and start it in placement mode so the user can -->
        <!-- choose a location for the object -->
        <a-entity zappar-face id="face-anchor">

            <!-- Include a 3D model inside our instant tracker -->
            <a-entity geometry="primitive: face-mesh; face: #face-anchor" material="src:url(assets/faceMeshTemplate.png); transparent: true;"></a-entity>

        </a-entity>
    </a-scene>
</body>

</html>
Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
