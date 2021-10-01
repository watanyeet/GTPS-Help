```cpp
This With GamePacket
if (cch.find("action|store") == 0) 
					{
						if (((PlayerInfo*)(peer->data))->haveGrowId == true)
						{
              GamePacket p2 = packetEnd(appendString(appendString(createPacket(), "OnDialogRequest"), "add_label_with_icon|big|`wWelcome to our store!``|left|5016|add_spacer|small|add_textbox|`rPlease choose item that you want to purchase!``|left|add_spacer|small|add_button_with_icon|purchaselist|Purchase items|noflags|7010|||add_button_with_icon||END_LIST|noflags|0||add_button_with_icon|storexp|XP-Boost|noflags|6880||add_button_with_icon|storeplace|Punch-Boost|noflags|6886|||add_button_with_icon||END_LIST|noflags|0||add_button_with_icon|purchasepet|Purchase PET|noflags|3554||add_button_with_icon|purchasebusiness|Purchase Business|noflags|2398||add_button_with_icon|investingerben|Investing|noflags|752|||add_button_with_icon||END_LIST|noflags|0||add_spacer|small|add_button|shoplist|`wMarketplace``|NOFLAGS|0|0|small|add_button|purchaseworldlock|`4GTPS:`` `9Premium Wls``|NOFLAGS|0|0|add_quick_exit|add_button|chc0|Close|noflags|0|0|\nend_dialog|gazette||OK|"));
							ENetPacket* packet2 = enet_packet_create(p2.data,
								p2.len,
								ENET_PACKET_FLAG_RELIABLE);
							enet_peer_send(peer, 0, packet2);

							delete p2.data;
							enet_host_flush(server);
						}

					}
          
          
          
This With Player Class 
if (cch.find("action|store") == 0) 
					{
						if (((PlayerInfo*)(peer->data))->haveGrowId == true)
						{
            Player::OnDialogRequest(peer, "add_label_with_icon|big|`wWelcome to our store!``|left|5016|add_spacer|small|add_textbox|`rPlease choose item that you want to purchase!``|left|add_spacer|small|add_button_with_icon|purchaselist|Purchase items|noflags|7010|||add_button_with_icon||END_LIST|noflags|0||add_button_with_icon|storexp|XP-Boost|noflags|6880||add_button_with_icon|storeplace|Punch-Boost|noflags|6886|||add_button_with_icon||END_LIST|noflags|0||add_button_with_icon|purchasepet|Purchase PET|noflags|3554||add_button_with_icon|purchasebusiness|Purchase Business|noflags|2398||add_button_with_icon|investingerben|Investing|noflags|752|||add_button_with_icon||END_LIST|noflags|0||add_spacer|small|add_button|shoplist|`wMarketplace``|NOFLAGS|0|0|small|add_button|purchaseworldlock|`4GTPS:`` `9Premium Wls``|NOFLAGS|0|0|add_quick_exit|add_button|chc0|Close|noflags|0|0|\nend_dialog|gazette||OK|");
            }           
          }
```          
