graph TD

    subgraph Core_Compute["Core Compute Layer"]
        NOVA["NOVA<br/>Peladn Mini PC<br/>Ubuntu + ROS 2 Jazzy + Piper"]
        Pedro["Pedro<br/>Windows Workstation<br/>CAD / Docs / Git"]
        Jose["Jose<br/>Dell Laptop<br/>Ubuntu + ROS 2 Jazzy"]
        HA["Home Assistant<br/>Peladn bare-metal<br/>Home automation"]
    end

    subgraph Indoor_Robots["Indoor Robots"]
        A1["Alfred 1<br/>Pi 5 + SSD<br/>JGA25-371 motors + TB6612FNG<br/>ROS 2 Jazzy"]
        A5["Alfred 5<br/>Pi 5 + SSD<br/>Wheelchair motors + IBT-2<br/>ROS  2 Jazzy"]
        Moe["Moe<br/>Adafruit Feather Rover"]
        Larry["Larry<br/>Pi Zero 2 W Rover"]
        Curly["Curly<br/>Pi 3B+ Rover"]
    end

    subgraph Outdoor_Robots["Outdoor Robots"]
        Oscar["Oscar<br/>Pi 5<br/>Hoverboard motors (zero-turn)<br/>ROS 2 Jazzy"]
    end

    subgraph IoT_Nodes["NOVAgrid Nodes & Special Units"]
        Skully["Skully<br/>Pi 4<br/>Rhasspy + Piper<br/>Animatronic skull"]
        Spyder["Arachno / Spyder<br/>ESP32-CAM<br/>Wi-Fi camera"]
        Nodes["NOVAgrid Sensor Nodes<br/>ESP32 / ESP01 / Picos / Arduinos"]
    end

    %% Core Relationships
    NOVA --- Jose
    NOVA --- HA
    Pedro --- NOVA
    Pedro --- Jose

    %% NOVA <-> Robots
    NOVA --- A1
    NOVA --- A5
    NOVA --- Moe
    NOVA --- Larry
    NOVA --- Curly
    NOVA --- Oscar

    %% NOVA <-> IoT
    NOVA --- Skully
    NOVA --- Nodes
    Skully --- Spyder
    HA --- Nodes

    %% Operators
    Jose --- A1
    Jose --- A5
    Jose --- Oscar
    Jose --- Larry
    Jose --- Curly
    Jose --- Moe
