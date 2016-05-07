# WaterDrop
Imitation QQ chat message which can drag remove air bubbles

#WaterDrop使用
初始化：
*    CoverManager.getInstance().init(this);
*		CoverManager.getInstance().setMaxDragDistance(150);
*		CoverManager.getInstance().setExplosionTime(150);


使用：调用waterdrop布局
*	  WaterDrop drop = (WaterDrop) convertView.findViewById(R.id.drop);
	    drop.setText(String.valueOf(position));
	  	drop.setOnDragCompeteListener(new OnDragCompeteListener() {

				@Override
				public void onDrag() {
					Toast.makeText(MainActivity.this, "remove:" + position,
							Toast.LENGTH_SHORT).show();
				}
			});
